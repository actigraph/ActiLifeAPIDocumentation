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
    <td>UseWTVData</td>
    <td>If enabled and the AGD file has them, ActiLife will filter non-wear time from the results.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>UseLogDiaries</td>
    <td>If enabled and the AGD file has them, ActiLife will only use log diary times. 
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
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
    <td>CalculateMETs</td>
    <td>If enabled, ActiLife will calculate MET results.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
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
    <td>CalculateBouts</td>
    <td>If enabled, ActiLife will calculate Bout results.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>CalculateSedentaryAnalysis</td>
    <td>If enabled, ActiLife will calculate Sedentary results.
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
    <td>IncludeDailyResults</td>
    <td>If enabled, daily results will be calculated for each algorithm.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>IncludeHourlyResults</td>
    <td>If enabled, hourly results will be calculated for each algorithm.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>EnergyExpenditureAlgorithm</a></td>
    <td>Options for energy expenditure algorithm to use.
        <p>Accepted Values:</p>
		<ul>
		    <li>WorkEnergy</li>
            <li>FreedsonSingleAxis</li>
            <li>FreedsonSingleCombination (default)</li>
            <li>FreedsonVM</li>
            <li>FreedsonVMCombination</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>METAlgorithm</a></td>
    <td>Options for MET algorithm to use.
        <p>Accepted Values:</p>
		<ul>
		    <li>FreedsonEEAdult (default)</li>
            <li>CrouterAdult</li>
            <li>FreedsonTreadmill1998Adult</li>
            <li>HendelmanOverground2000Adult</li>
            <li>HendelmanOvergroundLifestyle2000Adult</li>
            <li>SwartzOvergroundLifestyle2000Adult</li>
            <li>LeendersTreadmill2003Adult</li>
            <li>YngveTreadmill2003Adult</li>
            <li>YngveOverground2003Adult</li>
            <li>BrooksOverground2003Adult</li>
            <li>BrooksBodymassOverground2003Adult</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>CutPointSet</a></td>
    <td>Cut point set to use.
        <p>Accepted Values:</p>
		<ul>
		    <li>FreedsonAdult1998 (default)</li>
            <li>FreedsonAdultVM32001</li>
            <li>FreedsonChildren2005</li>
            <li>PuyauChildren2002</li>
            <li>TreuthChildrenGirls2004</li>
            <li>MattocksChildren2007</li>
            <li>EvensonChildren2008</li>
            <li>PatePreschool2006</li>
            <li>TrostToddler2011</li>
            <li>TroianoAdult2008</li>
            <li>PulsfordChildren2001</li>
            <li>ButtePreschoolersVM2013</li>
            <li>ButtePreschoolers2013</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
</table>

### Example Action

    {
        "Action": "DataScoring",
        "Args": {
            "FileInputPath": "c:\\input\\CLE2A123456789.agd",
            "UseWTVData": true,
       		"UseLogDiaries": false,
			"CalculateEnergyExpenditure": true,
			"EnergyExpenditureAlgorithm": "FreedsonSingleCombination",
			"IncludeExtraStatistics": true,
			"IncludeDailyResults": true
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
  
* [Energy Expenditure Results](elements/eeResults.md)
* [MET Results](elements/metResults.md)
* [Cut Point Results](elements/cutPointResults.md)
* [Bout Results](elements/boutResults.md)
* [Sedentary Results](elements/sedentaryResults.md)
* [Extra Stats Results](elemtns/statResults.md)