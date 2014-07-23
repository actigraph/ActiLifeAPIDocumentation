## CutPointOptions [API 1.10]

Options for a Cut Point Algorithms.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Calculate</td>
    <td>If enabled, ActiLife will calculate cut point results.
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
    <td>Which cut point algorithm to use
        <p>Accepted values:</p>
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
