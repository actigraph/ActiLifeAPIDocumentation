## METOptions [API 1.10]

Options for MET Algorithms.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
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
            <li>BrooksOverground2005Adult</li>
            <li>BrooksBodymassOverground2005Adult</li>
			<li>FreedsonChildren</li>
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
			<li>Weight is required for FreedsonEEAdult Algorithm</li>
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
  <tr>
    <td>Age</td>
    <td>Age of the subject in years.
        <p>Notes:</p>
        <ul>
			<li>Age is required for FreedsonChildren Algorithm (between 6 and 18)</li>
			<li>If an AGD already has an age, it is not necessary to pass in this parameter.</li> 
			<li>If the AGD doesn't have an age and no age is passed in, the calculation will return with an error.</li>
        </ul>
        <p>Restrictions:</p>
        <ul>
            <li>0-130 years</li>
        </ul>
    </td>
    <td>No</td>
    <td>int</td>
  </tr>
</table>
