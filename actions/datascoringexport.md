# DataScoringExport [API 1.12]

Calculate and Export Data Scoring Results for multiple files. This mimics the Data Scoring tab in ActiLife. Select the files, algorithms, and export type.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>FileInputPaths</td>
    <td>The source file(s) to calculate and export.
        <p>Accepted Input Formats:</p>
        <ul>
            <li>agd</li>
        </ul>
    </td>
    <td>Yes</td>
    <td>string[]</td>
  </tr>
  <tr>
    <td>ExportLocation</td>
    <td>The file or directory to export results.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td><a href="../elements/filterOptions.md">FilterOptions</a></td>
    <td>Options for which filters to use when calculating.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td>CalculateEnergyExpenditure</td>
    <td>If enabled, ActiLife will calculate energy expenditure results.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td><a href="../elements/eeOptions.md">EnergyExpenditureOptions</a></td>
    <td>Options for calculating energy expenditure results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td>CalculateMETs</td>
    <td>If enabled, ActiLife will calculate MET results.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td><a href="../elements/metOptions.md">METOptions</a></td>
    <td>Options for calculating METs results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td>CalculateCutPoints</td>
    <td>If enabled, ActiLife will calculate Cut Point results.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td><a href="../elements/cutPointOptions.md">CutPointOptions</a></td>
    <td>Options for calculating cut point results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td>CalculateBouts</td>
    <td>If enabled, ActiLife will calculate Bout results using the default ActiLife bout settings.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>CalculateSedentaryAnalysis</td>
    <td>If enabled, ActiLife will calculate Sedentary results using the default ActiLife sedentary settings.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>IncludeExtraStatistics</td>
    <td>If enabled, ActiLife will calculate extra statistics.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ExportFileType</td>
    <td>The type of export to use.
        <p>Accepted Values:</p>
        <ul><li>0 (Excel). This is the default</li><li>1 (CSV)</ul></td>
    </td>
    <td>true</td>
    <td>int/enum</td>
  </tr>
  <tr>
    <td><a href="../elements/batchExportSheetOptions.md">BatchExportSheetOptions</a></td>
    <td>The options for what to show in the export sheets.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
</table>

### Example Action
```JSON
{
  "Action": "DataScoringExport",
  "Args": {
    "FileInputPaths": [
      "C:\\Users\\john.doe\\desktop\\file.agd"
    ],
    "ExportLocation": "C:\\Users\\daniel.judge\\Documents\\export.xlsx",
    "BatchExportSheetOptions": {
      "AddDefinitionComments": false,
      "AddDefinitionWorksheet": true,
      "AddWtv": true,
      "ShowNonWear": false,
      "ShowSummary": true,
      "ShowDaily": true,
      "ShowHourly": true,
      "AddSleepScores": false,
      "ShowBoutDetails": true,
      "ShowSedentaryDetails": true
    },
    "ExportFileType": 0,
    "FilterOptions": {
      "UseWTVData": true,
      "UseLogDiaries": false
    },
    "CalculateEnergyExpenditure": true,
    "EnergyExpenditureOptions": {
      "Algorithm": "FreedsonSingleCombination"
    },
    "CalculateMETs": false,
    "METOptions": {
      "Algorithm": "FreedsonEEAdult"
    },
    "CalculateCutPoints": false,
    "CutPointOptions": {
      "Algorithm": "FreedsonAdult1998"
    },
    "CalculateBouts": true,
    "CalculateSedentaryAnalysis": true,
    "IncludeExtraStatistics": true
  }
}
```

## Response

### Example Response
```JSON
{
    "Response": "DataScoringExport",
    "Success": true,
    "Error": "",
    "Args": { ... }
}
```