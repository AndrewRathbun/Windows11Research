# Enumerating Available Event Logs in Windows 11

Run the following command in PowerShell (Admin):

```PowerShell
(Get-WinEvent -ListLog *) | Select-Object -Property * | Export-Csv -path Windows11Events.csv -NoTypeInformation
```
