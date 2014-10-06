# CreateClinicalReport [API 1.11]

Calculate clinical report for a single AGD file.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>FileInputPath</td>
    <td>The source file to convert.
        <p>Accepted Input Formats:</p>
        <ul>
            <li>agd</li>
        </ul>
    </td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td><a href="../elements/clinicalreportoptions.md">ClinicalReportOptions</a></td>
    <td>Options for creating a clinical report.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
</table>

### Example Action
```JSON
{
  "Action": "CreateClinicalReport",
  "Args": {
    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd",
    "ClinicalReportOptions": {
      "WtvPageOn": true,
      "WtvAlgorithmName": "Troiano",
      "EnergyExpenditurePageOn": true,
      "EnergyExpenditureFormulaName": "FreedsonSingleCombination",
      "MetPageOn": true,
      "MetFormulaName": "FreedsonEEAdult",
      "CutPointPageOn": true,
      "CutPointSetName": "FreedsonAdult1998",
      "SleepGraphPageOn": true,
      "SleepTablePageOn": true,
      "SleepAlgorithm": "Sadeh",
      "TitlePageOn": true,
      "InterpretationPageOn": true,
      "LogDiaryOn": false
    }
  }
}
```

## Response

### Example Response
```JSON
{
  "Response": "CreateClinicalReport",
  "Success": true,
  "Error": "",
  "Args": {
    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd"
  },
  "Payload": {
    "ReportFileName": "c:\\users\\john.doe\\Desktop\\fileClinicalReport.pdf"
  }
}
```
