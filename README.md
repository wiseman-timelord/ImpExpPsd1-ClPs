# ImpExpPsd1-Ps

### STATUS
Development. Early version, do not use. The principles are...
- Testing, ensure the cmdlets work for, "PowerShell Core 7" and "Powershell 5.1", ensure everything is compatible.
- we ideally want them to work more, competently and faster, than the PowerShell/PowerShellCore versions of the relating cmdlets, no security or error handling, the data will be trusted to be, correct from the export and safe (non-executable) due to the relating program.
- we want them to utilize exactly the same, syntax and usage, for import, and a fitting theme of, syntax and usage, for the export, compared to the powershell import.
- after the scripts have been, tested and improved, though use in my programs (starting with [BethScale](https://github.com/wiseman-timelord/DdsBethScale-PsWhile)), then functions will be converted to c# cmdlets, and additionally put on [PowerShellGallery](https://www.powershellgallery.com/packages/). 

## DESCRIPTION
Powershell and PowerShellCore do not have an Export-PowerShellDataFile cmdlet, therein, every time the given user attemts to use a Psd1 with a script created in GPT4, then it will cause a series of different errors in development to happen, that are frustrating interactions if you intend to use Psd1, hence, I wanted to solve that issue, and not only that, but produce upgrades in the process. ImpExpPsd1-Cl will fix the issue of incorrectly reading/writing to PSD1's with perfected, import and export, functions and cmdlets, that are, robust and efficient, hence, "Import Export Psd1", functions (cmdlets later too) was created for exactly this purpose.

### DEMONSTRATION
- Some GPT4 logic upon exporting Psd1 files (in a new session - 2024/01/24)...
```
WT:
Powershell and PowerShellCore do not have an Export-PowerShellDataFile cmdlet, is this, true or false?

GPT4:
The statement is false. Both PowerShell and PowerShell Core do include the `Export-PowerShellDataFile` cmdlet...
...
```
- Standard Psd1 import has issues...
```
WT:
Please tell me about the, limitations and issues, of Import-PowerShellDataFile.

GPT4: 
...
Handling Complex Data: While it can import nested hashtables or custom objects, the complexity of the data structure can lead to confusion or errors in interpretation.
...
```

## USAGE
1. Install/Import the, script or cmdlet. 
2. Depend on the circumstance...The, syntax and usage, of the import will work the same as the built-in one, hence, you just need to swap the cmdlet names. For export, the, syntax and usage, of the export is as GPT hallucinated it to be, so under such circumstances, it may again be a case of swapping function/cmdlet names.
- Import...
```
$ConfigData = Import-PowerShellData1 -Path "C:\path\to\config.psd1"

$Setting1Value = $ConfigData.Setting1
```
- Export...
```
$data = @{
    Setting1 = 'Value1'
    Setting2 = 'Value2'
}

$data | Export-PowerShellData1 -Path 'C:\path\to\your\file.psd1'
```

### NOTATION
- There is a "Export-PowerShellDataFile" on GitHub, however, mine will be, better than, that cmdlet and the standard "Import-PowerShellDataFile" cmdlet. The GitHub export psd cmdlet is [here](https://github.com/rhubarb-geek-nz/PowerShellDataFile/), its v1.0 currently.

## DISCLAIMER
This software is not subject to the terms in my typically supplied License.Txt, as it is NOT an actual program. I want users to use these files HOWEVER they want, I am just trying to fix a blatant FATAL ERROR in PowerShell/PowerShellCore. Obviously if your computer blows up, then you must accept, that is more likely to be the box of TNT yer left on top of it.


