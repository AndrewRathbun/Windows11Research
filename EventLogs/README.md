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

## Enumerating Event Log Providers by Name Only

Run the following command in PowerShell (Admin):

```PowerShell
(Get-WinEvent -ListLog *).OwningProviderName
```
## Enumerating Event Logs by Provider, Event ID, and Event Description

```PowerShell
 Get-WinEvent -LogName * | Select-Object -Property ProviderName, Id, Message | Export-Csv Windows11EventsProviderIDDescription.csv -NoTypeInformation
```

*awaiting test to complete*
