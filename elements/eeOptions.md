## EnergyExpenditureOptions [API 1.10]

Options for Energy Expenditure Algorithms.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
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
  <tr>
    <td>Weight</td>
    <td>Weight of the subject in kilograms.
        <p>Notes:</p>
        <ul>
			<li>If an AGD already has a weight, it is not necessary to pass in this parameter.</li> 
			<li>If the AGD doesn't have a weight and no weight is passed in, the calculation will return with an error.</li>
        </ul>
        <p>Restrictions:</p>
        <ul>
            <li>0 - 2000 kg</li>
        </ul>
    </td>
    <td>No</td>
    <td>float</td>
  </tr>
</table>
