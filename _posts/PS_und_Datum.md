Notizen zu Powershell und Datum als Datentyp und Funktion.  

Cmdlet "Get-Date" ist zuständig für Datumsinformationen. Mit ```get-date | get-member``` können die Funktionen aufgelistet werden. Z.B. ```(get-date).month```.  Alternativ kann man über eine Variable gehen:  

```
$datum = Get-Date
$datum.month
```

In Powershell sind alles Objekte. D.h. $datum ist keine Variable, sondern ein Objekt. Daher kann über die Variable die gleichen Methoden angewendet werden. Ich kann dem Objekt auch ein konkretes Datum vorgeben und z.B. fragen, was für ein Wochentag das es ist  

![get-culture](..\powershell\get-culture.png)  



# Codesnippets



## Jahrestag in Datum konvertieren

```
$TempDate = ([datetime]"01/01/$((Get-Date).Year)").AddDays(140-1) $ShortDate = 
$TempDate.ToShortDateString()
```

# Quellen

* [WindowsPro.de: Get-Date: Datum berechnen und formatieren in Powershell](https://www.windowspro.de/script/datum-berechnen-formatieren-powershell-get-date)  
* [Microsoft Docs: Get-Date](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/get-date?view=powershell-6)  
* 