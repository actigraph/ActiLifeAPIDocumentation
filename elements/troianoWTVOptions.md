## TroianoWTVOptions

<table>
  <tr>
    <th>Element</th>
    <th>Description</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>MinimumLengthUnits</td>
    <td></td>
	<td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>UseActivityThreshold</td>
    <td></td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ActivityThreshold</td>
    <td></td>
    <td>int</td>
  </tr>
  <tr>
    <td>ActivityThresholdUnits</td>
    <td></td>
    <td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>UseMaxCount</td>
    <td></td>
    <td>bool</td>
  </tr>
  <tr>
    <td>MaxCount</td>
    <td></td>
    <td>int</td>
  </tr>
  <tr>
    <td>MaxCountUnits</td>
    <td></td>
    <td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>SpikeTolerance</td>
    <td></td>
    <td>int</td>
  </tr>
  <tr>
    <td>SpikeToleranceUnits</td>
    <td></td>
    <td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>UseCountsToStopNonWearPeriod</td>
    <td></td>
    <td>bool</td>
  </tr>
  <tr>
    <td>CountsToStopNonWearPeriod</td>
    <td></td>
    <td>int</td>
  </tr>
  <tr>
    <td>CountsToStopNonWearPeriodUnits</td>
    <td></td>
    <td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>UseConsecutiveEpochs</td>
    <td></td>
    <td>bool</td>
  </tr>
  <tr>
    <td>MinimumLength</td>
    <td>The minimum length of a non-wear period</td>
    <td>int</td>
  </tr>
  <tr>
    <td>VM</td>
    <td>If set to true (and the file has 3 axis data), vector magnitude will be used</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>UseIgnoreShortWearPeriods</td>
    <td>If set to true, wear periods must be a certain length to be valid</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShortWearPeriodsLength</td>
    <td>Wear Periods at or below this value will be ignored and converted to non-wear time</td>
    <td>int</td>
  </tr>
  <tr>
    <td>ShortWearPeriodsUnits</td>
    <td>The units for the short wear periods (minutes or epochs)</td>
    <td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>UseMinimumWearTimePerDay</td>
    <td>If set to true, require a minimum amount of wear per day.</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>MinimumWearTimePerDayLength</td>
    <td>If the amount of wear for a calendar day is below the specified level, the entire day will be converted to non-wear</td>
    <td>int</td>
  </tr>
  <tr>
    <td>MinimumWearTimePerDayUnits</td>
    <td>The units for the minimum wear time per day (minutes or epochs).</td>
    <td><a href="../elements/boutUnits.md">Units</a></td>
  </tr>
  <tr>
    <td>UseMinimumDaysOfValidWearTime</td>
    <td>If set to true (and UseMinimumWearTimePerDay is true), require a specified number of days with wear time.</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>MinimumDaysOfValidWearTime</td>
    <td>The number of days with valid wear time required to make a data set required. If a dataset doesn't have the specified number of days, the entire file will be set to non-wear</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Sleep</td>
    <td>Controls if sleep periods should be used in this bout setting.</td>
	<td><a href="../elements/SleepPeriodWTVOption.md">SleepPeriodWTVOption</a></td>
  </tr>
</table>



