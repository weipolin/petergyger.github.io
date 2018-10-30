# Win10 Home optimieren

## Gruppenrichtlinien Editor aktivieren

Admin CLI:  

Wenn die For Schlaufe in einem Batch (.CMD / .BAT) verwendet wird, muss das Prozentzeichen der Variabel (%i) verdoppelt (%%1) werden

dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt  
dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt  
  
for /f %i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%i"  

## HyperV installieren

Hardware Anfoderungen prüfen. Admin CLI:  
  
dir /b %SystemRoot%\servicing\Packages\*Hyper-V*.mum >hyper-v.txt  
  
for /f %i in ('findstr /i . hyper-v.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%i"  
  
del hyper-v.txt  
  
Dism /online /enable-feature /featurename:Microsoft-Hyper-V-All /LimitAccess /ALL  



