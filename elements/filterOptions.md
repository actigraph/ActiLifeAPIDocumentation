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
</table>
