## FilterOptions [API 1.10]

Options for which filters to use for data scoring.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>UseWTVData</td>
    <td>Enable this option to exclude non-wear data periods from analysis. This does not perform the non-wear analysis.  The non-wear analysis must already be present in the AGD file; otherwise this option is ignored and all data is considered wear.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>UseLogDiaries</td>
    <td>Enable this option to only include log diary periods from analysis. This does not allow you to add log diaries. The log diaries must already be present in the AGD file. If UseWTVData and UseLogDiaries are both selected (and the file has both) the analysis will only include the overlapping periods of wear periods and log diaries.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
</table>
