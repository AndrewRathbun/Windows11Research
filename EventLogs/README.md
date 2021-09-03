# Useful PowerShell Commands


## Enumerating Available Event Logs in Windows 11

Run the following command in PowerShell (Admin):

```PowerShell
(Get-WinEvent -ListLog *) | Select-Object -Property * | Export-Csv -path Windows11Events.csv -NoTypeInformation
```

## Enumerating Event Log Channels by Name Only

Run the following command in PowerShell (Admin):

```PowerShell
(Get-WinEvent -ListLog *).LogName
```
Note: Does not appear to include Security, System, etc.

## Enumerating Even Log Providers by Name Only

Run the following command in PowerShell (Admin):

```PowerShell
(Get-WinEvent -ListLog *).OwningProviderName
```
