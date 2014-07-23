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
    <td><a href="../elements/filtereOptions.md">FilterOptions</a></td>
    <td>Options for which filters to use when calculating.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
    <tr>
    <td><a href="../elements/eeOptions.md">EnergyExpenditureOptions</a></td>
    <td>Options for calculating energy expenditure results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/metOptions.md">METOptions</a></td>
    <td>Options for calculating METs results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/cutPointOptions.md">CutPointOptions</a></td>
    <td>Options for calculating cut point results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/boutOptions.md">BoutOptions</a></td>
    <td>Options for calculating bout results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/sedentaryOptions.md">SedentaryOptions</a></td>
    <td>Options for calculating sedentary results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/statsOptions.md">ExtraStatisticsOptions</a></td>
    <td>Options for calculating extra AGD statistic results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/resultOptions.md">ResultOptions</a></td>
    <td>Options for which results to return.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>  
</table>

### Example Action

    {
        "Action": "DataScoring",
        "Args": 
		{
            "FileInputPath": "c:\\input\\CLE2A123456789.agd",
			"FilterOptions": 
			{
				"UseWTVData": true,
       			"UseLogDiaries": false
			}
			"EnergyExpenditureOptions": 
			{
				"Calculate": true,
				"EnergyExpenditureAlgorithm": "FreedsonSingleCombination"
			}
			"ResultOptions":
			{
				"IncludeTotalResults": true,
				"IncludeExtraStatistics": true,
				"IncludeDailyResults": true
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