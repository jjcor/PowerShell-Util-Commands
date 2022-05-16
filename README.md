# PowerShell-Util-Commands
Get proccesese shorted by CPU of a domain machine
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock {Get-Process | Sort-Object CPU -Descending}
```
Add domain user, to a local admin group of AD machine.
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock {add-localgroupmember -Group 'Administradores' -Member 'south\maq'}
```
Remove domain user, to a local admin group of AD machine.
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock {remove-localgroupmember -Group 'Administradores' -Member 'south\maq'}
```
Remove dameware agent of AD machine
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock { net stop dwmrcs }
```
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock { C:\Windows\dwrcs\dwrcs.exe -remove }
```
