# ClinicalReportOptions [API 1.11]

Options for creating a clinical report

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>WtvPageOn</td>
    <td>If set to true, the clinical report will calculate and show wear time validation information.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>WtvAlgorithmName</td>
    <td> The wear time validation algorithm to use.
        <p>Accepted Values:</p>
        <ul>
			<li>Troiano (default)</li>
			<li>Choi</li>
			<li>Daily</li>
		</ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>EnergyExpenditurePageOn</td>
    <td>If set to true, the clinical report will calculate and show energy expenditure information.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>EnergyExpenditureFormulaName</td>
    <td>The energy expenditure formula to use for the clinical report.
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
    <td>MetPageOn</td>
    <td>If set to true, the clinical report will calculate and show MET rate information.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>MetFormulaName</td>
    <td>The MET formula to use for the clinical report.
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
    <td>CutPointPageOn</td>
    <td>If set to true, the clinical report will calculate and show cut point information.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>CutPointSetName</td>
    <td>The cut point set to use for the clinical report.
        <p>Accepted values:</p>
        <ul>
            <li>FreedsonAdult1998 (default)</li>
            <li>FreedsonAdultVM32011</li>
            <li>FreedsonChildren2005</li>
            <li>PuyauChildren2002</li>
            <li>TreuthChildrenGirls2004</li>
            <li>MattocksChildren2007</li>
            <li>EvensonChildren2008</li>
            <li>PatePreschool2006</li>
            <li>TrostToddler2011</li>
            <li>TroianoAdult2008</li>
            <li>PulsfordChildren2011</li>
            <li>ButtePreschoolersVM2013</li>
            <li>ButtePreschoolers2013</li>
		</ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>SleepGraphPageOn</td>
    <td>If set to true, the clinical report will calculate and show a dual plot for each calendar day with sleep information.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>SleepTablePageOn</td>
    <td>If set to true, the clinical report will calculate and show a table of sleep scores.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>SleepAlgorithm</td>
    <td>Sleep algorithm to use in the clinical report.
        <p>Accepted Values:</p>
        <ul>
			<li>Troiano (default)</li>
			<li>Choi</li>
			<li>Daily</li>
		</ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>TitlePageOn</td>
    <td>If set to true, the clinical report will show a title page.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>InterpretationPageOn</td>
    <td>If set to true, the clinical report will calculate and show a box for interpretation on the last page.
        <p>Accepted Values:</p>
        <ul><li>true (default)</li><li>false</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>LogDiaryOn</td>
    <td>If set to true, the clinical report will use log diary times when calculating energy expenditure and cut points.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
</table>
