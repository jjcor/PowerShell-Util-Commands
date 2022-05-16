# PowerShell-Util-Commands
Get proccesese shorted by CPU of a domain machine
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock {Get-Process | Sort-Object CPU -Descending}
```
Añadir usuario del dominio a grupo administradores local
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock {add-localgroupmember -Group 'Administradores' -Member 'south\maq'}
```
Quitar usuario del dominio a grupo administradores local
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock {remove-localgroupmember -Group 'Administradores' -Member 'south\maq'}
```
Quitar agente Dameware a una maquina en remoto
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock { net stop dwmrcs }
```
```powershell
Invoke-Command -ComputerName PC-00X -ScriptBlock { C:\Windows\dwrcs\dwrcs.exe -remove }
```
