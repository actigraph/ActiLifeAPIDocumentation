## EnergyExpenditureOptions [API 1.10]

Options for a Energy Expenditure Algorithms.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Calculate</td>
    <td>If enabled, ActiLife will calculate energy expenditure results.
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
    <td>Which energy expenditure algorithm to use
        <p>Accepted values:</p>
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
</table>
