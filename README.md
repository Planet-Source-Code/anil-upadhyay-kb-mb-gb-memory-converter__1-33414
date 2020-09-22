<div align="center">

## KB/MB/GB memory converter


</div>

### Description

Change bytes to KB/MB/GB to 2 decimal places
 
### More Info
 
Input - Long value (Bytes)

Ouput - KB/MB/GB to 2 decimal places

None yet


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Anil Upadhyay](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/anil-upadhyay.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Math/ Dates](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math-dates__1-37.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/anil-upadhyay-kb-mb-gb-memory-converter__1-33414/archive/master.zip)





### Source Code

```
Public Function convertmeg(HDD As Long)
'Convert to Kb/MB/GB
Dim counter, unitcounter As Integer
Dim HDDasD As Double 'hdd as double conversion required for decimals
Dim unit As String 'bytes, kb, mb, gb
unitcounter = 0
HDDasD = HDD
'Loop
For counter = 0 To 3
  If HDDasD > 1024 Then
  HDDasD = (HDDasD / 1024)
  unitcounter = unitcounter + 1
  End If
Next
If unitcounter = 0 Then unit = "Bytes"
If unitcounter = 1 Then unit = "KB"
If unitcounter = 2 Then unit = "MB"
If unitcounter = 3 Then unit = "GB"
HDDasD = Format(HDDasD, "#0.00")  '2 decimal places
convertmeg = HDDasD
End Function
```

