# DataScoring [API 1.10]

Get data scoring algorithm results for a single AGD file.

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
    <td><a href="../elements/dataScoringResultOptions.md">DataScoringResultOptions</a></td>
    <td>Options for which results to return.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>  
</table>

### Example Action

    {
	  "Action": "DataScoring",
	  "Args": {
	    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd",
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
	    "CalculateBouts": false,
	    "CalculateSedentaryAnalysis": false,
	    "IncludeExtraStatistics": false,
	    "DataScoringResultOptions": {
	      "IncludeTotalResults": true,
	      "IncludeDailyResults": false,
	      "IncludeHourlyResults": false
	    }
	  }
	}

## Response

### Example Response

    {
        "Response": "DataScoring",
        "Success": true,
        "Error": "",
        "Args": { ... }
    }

### Detailed Response
  
* [Energy Expenditure Results](../elements/eeResults.md)
* [MET Results](../elements/metResults.md)
* [Cut Point Results](../elements/cutPointResults.md)
* [Bout Results](../elements/boutResults.md)
* [Sedentary Results](../elements/sedentaryResults.md)
* [Extra Stats Results](../elements/statResults.md)