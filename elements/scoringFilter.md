## ScoringFilter [API 1.12]

A global date/time filter. Used in Data Scoring calculations.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Type</td>
    <td>The type of filter to use.
        <p>Accepted values:</p>
        <ul>
            <li>0 (AllDays - Filter applies to every day of data)</li>
			<li>1 (Weekdays - Filter applies to only weekdays)</li>
			<li>2 (Weekends - Filter applies to only weekends)</li>
			<li>3 (DayOfTheWeek - Filter applies to only a specific day of the week)</li>
			<li>4 (SpecificDate - Filter applies to a specific date)</li>
			<li>5 (DayRange - Filter applies to a day range - i.e. Tuesday through Friday)</li>
			<li>6 (DateRange - Filter Applies to a date range - i.e. 2015-03-29 through 2015-04-10)</li>
		</ul>
    </td>
    <td>int/enum</td>
  </tr>
  <tr>
    <td>Name</td>
    <td>The name for this filter.</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Use</td>
    <td>If set to true, this filter will be used. If false, it won't be used.</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>StartTime</td>
    <td>The start time of the filter (only uses the TimeOfDay property of this value).</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>StopTime</td>
    <td>The stop time of the filter (only uses the TimeOfDay property of this value).</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>DayOfTheWeek</td>
    <td>Day of the week number.  0 is Sunday, 1 is Monday ... 6 is Saturday.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>DayRangeStart</td>
    <td>If using the DayRange filter, set this for the start day to the day of the week number. 0 is Sunday, 1 is Monday ... 6 is Saturday.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>DayRangeEnd</td>
    <td>If using the DayRange filter, set this for the end day to the day of the week number. 0 is Sunday, 1 is Monday ... 6 is Saturday.</td>
    <td>string</td>
  </tr>
  <tr>
    <td>SpecificDate</td>
    <td>If using the SpecificDate filter, set this for the date to use. It ignores any Time portion of the DateTime.</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>DateRangeStart</td>
    <td>The name for this filter.</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>DateRangeEnd</td>
    <td>The name for this filter.</td>
    <td>DateTime</td>
  </tr>
</table>
