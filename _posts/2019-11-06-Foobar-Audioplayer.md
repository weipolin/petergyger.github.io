In der Windowswelt hat man die grösste Auswahl an Software. [Foobar2000](http://www.foobar2000.org) ist seit 2002 der Audioplayer für Nerds. Wobei Player irreführend ist, da auch CDs gerippt werden können, Tags editiert, etc. Der spartanischen Oberfläche stehen die ausgefeilten Funktionen gegenüber. Die Software kann kostenlos genutzt werden und ist "closed Source". Jedoch hat der Entwickler Peter Pawloski ein umfangreiches Entwicklerpaket unter BSD Lizenz veröffentlicht. Daher hat es eine grosse Auswahl an Zusatzsoftware (Plugins). Ein weiterer Pluspunkt ist die sehr weitgehende Konfigurationsmöglichkeiten dieses Tools. Und - last but not least - die Kommandozeile (CLI) wird unterstützt.

Wie immer ist auch dieser Post aus meiner Praxis und bezogen auf die aktuelle Version 1.4 unter Windows 10 (Build 17134.345).  

# Was dazu gehört und in diesem Post nicht der Platz dafür ist

Das Ziel des Postes ist es, dass Tool Foobar2000 aus meiner Praxis vorzustellen. Vorgängig sollte man die eigene Antwort auf folgende Fragen gefunden haben:  

* Dateien benennen und Ordnerstruktur wie (Nomenklatura) anlegen?  
** Wenn ein Album aus mehr als einem Datenträger besteht, die Dateien in separaten Verzeichnissen ablegen?
** Namen: Maximale Länge und welche Zeichensätze?  
** Sich an veröffentlichten Datenträgern (CD) orientieren? Wenn ja, wie mit Bootleg, Onlineveröffentlichungen, etc. umgehen?  
* Welches Dateiformat (MP3 / FLAC / ETC.)?  
* Tags: Welche Tags nutzen? Welche Informationen sollen in den Tags abgelegt werden?
* Welche Geräte / Betriebssyteme / Applikationen / Netzprotokolle sollen Zugriff auf die Musik erhalten?
* ...

# Installation  

Man hat die Wahl zwischen einer portablen ![portablen](..\foobar\install.png)und einer Vollinstallation für alle Windowsbenutzer. Der Unterschied ist, dass die Verknüpfung- mit Dateierweiterungen nur in der Vollinstallation erfolgt. 
 Die [Installationsoptionen](http://wiki.hydrogenaud.io/index.php?title=Foobar2000:Components#Included_in_the_installer) sind i.d.R. für die allermeisten Fälle sinnvoll und beanspruchen wenig Resourcen:  

![Optionen](..\foobar\install-option.png)  

# Musik abspielen

Der nächste Schritt ist nun Foobar so zu konfigurieren, dass er die digitale Musik "findet". Der darauf folgende Schritt wird die Oberfläche sein, wo man viele gestalterische Freiheiten und Zusatzsoftware hat.

Mit der installierten Version von Foobar kann man wie folgt die Musikdateien laden:  
*  Datei abspielen: Rechtsklick auf die Datei (MP3 / Flac), Menupunkt "Öffnen mit" anklicken und Foobar2000 auswählen
*  Datei mit Foobar verknüpfen: Wie oben. Jedoch diesmal "Andere App auswählen" anklicken. Foobar2000 auswählen und den Haken "Immer diese..." setzen.  ![Windows](..\foobar\dateityp.png)  
*  Mit Foobar2000 direkt  
   1. Über den Menupunkt "File"   ![FileMenu](..\foobar\filemenu.png)
   2. Über die Medienbibliothek (nachdem sie eingerichtet ist)  ![FileMenu](..\foobar\library.png)
   3- Über Shortcuts. Default ist auf [Hydrogenaudio](https://wiki.hydrogenaud.io/index.php?title=Foobar2000:Preferences:General:Keyboard_Shortcuts#Key) dokumentiert.  
   1. CLI (cmd.exe / Powershell). Doku ist auf [Hydrogenaudio](https://wiki.hydrogenaud.io/index.php?title=Foobar2000:Commandline_Guide) zu finden.  

## Musikdatenbank

Das anlegen der Musikdatenbank ist die Grundlage der effizienten Nutzung von Foobar2000. Wer einfach nur seinen Künstler oder bestimmte Alben hören will, wird ohne glücklich. Dem Sammler bzw. Geniesser der in seinen Schätzen baden will, analog Dagobert Duck in seinen Dukaten, muss eine Datenbank erstellen. Über "Library", Untermenupunkt "Configure" gelangt man auf die Konfigurationsseite.  

![Preferences](..\foobar\preferences.png)  

Im Abschnitt "MusiC folders" sind die Verzeichnisse anzugeben, die danach Foobar2000 selbständig aktualisiert. Solange in der Spalte "Pending" steht, verarbeitet Foobar2000 noch die Musiksammlung. Im Abschnitt "File types" stehen keine Einträge, da ich in der Musiksammlung nur zwei Dateitypen ("Flac" / "MP3") habe. Im Abschnitt "Library viewer selection playlist" aktiviere ich "enabled". Dadurch wird automatisch eine Playliste über alle Musikstücke in der Library erstellt. Die Konfiguration mit "OK" bestätigen.  

Über die Komponente "Album List" (Menu "Library") wird der Inhalt der Datenbank als Verzeichnisbaum dargestellt. Im Menupunkt "View" kann die Sortierung bestimmt werden. Die Struktur dieser Abfragesprache wird in diesem Artikel von [audiohq](https://www.audiohq.de/viewtopic.php?id=1089) erklärt.  
![](foobar/album-list.png)






# Quellen

* [Foobar.org: FAQ](https://www.foobar2000.org/FAQ)
* [Deutsches Foobar Forum](http://foobar-users.de/index.php)
* [HydrogenAudio](https://hydrogenaud.io/index.php?PHPSESSID=e5or8l3adon8cu3m59rj1l51p6&board=28.0)
* [Reddit](https://www.reddit.com/r/foobar2000/)