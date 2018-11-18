Dieser Post beschreibt das Vorgehen, um mit Powershell folgenden Use Case abzudecken. Es wird überprüft, ob in einem Verzeichnis (Eingang) eines oder mehrere Dokumente existieren. Wenn ja, werden die Dokumente in ein anderes Verzeichnis verschoben, für jeden Monat ein anderes Verzeichnis. Mit dem verschieben wird das Dokument umbenannt. D.h. das Dokument erhält einen Prefix "xy-", wobei "xy-" für eine Zahl zwischen 1 und 20 steht. Wenn bereits Dokumente in diesem Folder sind, wird ermittelt welches die nächste freie Zahl ist. Es wird keine Fehlerroutine für den Fall das 20 Dokumente im Verzeichnis sind erstellt.  

Teil 1
# Eingangsverzeichnis auf Dokumente überprüfen.
# Verzeichnis des Eingages setzen. Danach Anzahl Einträge ermittlen
$folderinput="Z:\Peter\005 Beruf\Bewerbung\Chronologie\000 Eingang";
Get-ChildItem -Path $folderinput -File | Measure-Object | %{$_.Count}

# Monat ermitteln
$datum = Get-Date
# Zielverzeichnis gleich Monat in Zahl (Jan =1 / Feb = 2 / etc.). Danach nach Namen sortiert die letzte Datei anzeigen.
$folderoutput="Z:\Peter\005 Beruf\Bewerbung\Chronologie\" + $datum.Month;
$test = Get-ChildItem -Path $folderoutput | select name, state -last 1
$test.Split([char]3)


# Verzeichnis des Eingages setzen
$folderinput="Z:\Peter\005 Beruf\Bewerbung\Chronologie\000 Eingang";
Get-ChildItem -Path $folderinput
# $folderinput.count
# Monat ermitteln
$datum = Get-Date
# Zielverzeichnis gleich Monat in Zahl (Jan =1 / Feb = 2 / etc.)
$folderoutput="Z:\Peter\005 Beruf\Bewerbung\Chronologie\" + $datum.Month;
$test = Get-ChildItem -Path $folderoutput | select name, state -last 1