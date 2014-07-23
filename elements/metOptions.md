## METOptions [API 1.10]

Options for a MET Algorithms.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Calculate</td>
    <td>If enabled, ActiLife will calculate MET results.
        <p>Accepted values:</p>
        <ul>
            <li>true</li>
            <li>false (default)</li>
		</ul>
    </td>
    <td>Yes</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Algorithm</td>
    <td>Which MET algorithm to use
        <p>Accepted values:</p>
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
</table>
