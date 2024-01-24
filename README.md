# WtImpExpPsd1-Cl

## DESCRIPTION
Powershell and PowerShellCore do not have an Export-PowerShellDataFile cmdlet, GPT4 typically insists there is "GPT: The statement is false. Both PowerShell and PowerShell Core do include the Export-PowerShellDataFile cmdlet.", therein, every time the given user attemts to use a Psd1 with a script created in GPT4, then this will happen, wasting multiple frustrating interactions, hence, I wanted to solve that issue, and not only that, fix the issue of incorrectly reading/writing to PSD1's with quality, import and export, cmdlets, I can rely upon and are efficient, hence, "Wiseman-Timelord's Import Export Psd1" cmdlets were created for exactly this purpose. 

### DEMONSTRATION
- Some GPT4 logic upon exporting Psd1 files...
```
WT:
Powershell and PowerShellCore do not have an Export-PowerShellDataFile cmdlet, is this, true or false?

GPT4:
The statement is false. Both PowerShell and PowerShell Core do include the `Export-PowerShellDataFile` cmdlet. This cmdlet is used to export a hash table or a PSCustomObject to a PowerShell data file (*.psd1). The data file created by this cmdlet can be used in PowerShell scripts and modules to store data like configuration settings.

Here's a basic example of how you might use `Export-PowerShellDataFile`:

# Create a hash table
$data = @{
    Setting1 = 'Value1'
    Setting2 = 'Value2'
}

# Export the hash table to a PowerShell data file
$data | Export-PowerShellDataFile -Path 'C:\path\to\your\file.psd1'

This will create a file at the specified path containing the data from the hash table in a format that is easily readable and importable by PowerShell.
```
