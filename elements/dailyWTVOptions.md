## DailyWTVOptions


<table>
  <tr>
    <th>Element</th>
    <th>Description</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>MinHours</td>
    <td>Minimum number of wear hours in a day to be considered a valid day.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>MinDays</td>
    <td>Minimum number of days of wear time to be considered a valid data set.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>MinWeekDays</td>
    <td>Minimum number of weekdays of wear time to be considered a valid data set.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>MinWeekend</td>
    <td>Minimum number of weekend days of wear time to be considered a valid data set.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>UseMinZeros</td>
    <td>If true, the algorithm uses consecutive minutes of zeros to detect non-wear time.</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>MinZeros</td>
    <td>The number of consecutive minutes of zeros in an hour to be considered non-wear.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>UsePercent</td>
    <td>If true, the algorithm uses the percent of non-zero epochs per hour algorithm to detect non-wear time.</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Percent</td>
    <td>The percentage of non-zero epochs in a hour to be considered non-wear.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>IgnoreCountsBelow</td>
    <td>Counts at or below this number will be considered non-wear.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>IgnoreCountsAbove</td>
    <td>Counts at or above this number will be considered non-wear.</td>
    <td>int</td>
  </tr>
</table>