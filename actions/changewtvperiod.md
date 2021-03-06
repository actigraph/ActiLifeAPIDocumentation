# ChangeWearTimeValidationPeriod [API 1.11]

Change a wear time validation period from wear to non-wear or vice versa.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>FileInputPath</td>
    <td>The source file to convert.
        <p>Accepted Input Formats:</p>
        <ul>
            <li>agd</li>
        </ul>
    </td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>StartDateTime</td>
    <td>The start date/time of the period to change.</td>
    <td>Yes</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>StopDateTime</td>
    <td>The stop date/time of the period to change.</td>
    <td>Yes</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>IsWearPeriod</td>
    <td>Whether you want the period to be wear or not.</td>
    <td>Yes</td>
    <td>bool</td>
  </tr>
</table>

### Example Action
```JSON
{
  "Action": "ChangeWearTimeValidationPeriod",
  "Args": {
    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd",
	 "StartDateTime": "2014-10-01T05:00:00Z",
    "StopDateTime": "2014-10-01T06:00:00Z",
	"IsWearPeriod": false
  }
}
```

## Response

### Example Response
```JSON
{
  "Response": "ChangeWearTimeValidationPeriod",
  "Success": true,
  "Error": "",
  "Args": {
    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd",
    "Algorithm": "Choi"
  },
  "Payload": {
    "Filename": "c:\\users\\john.doe\\Desktop\\file.agd",
    "Periods": [
      {
        "CalendarDays": 4,
        "LengthInMinutes": 4974.0,
        "IsWearPeriod": true,
        "StartDateTime": "2009-10-05T11:00:00",
        "StopDateTime": "2009-10-08T21:54:00"
      },
      {
        "CalendarDays": 2,
        "LengthInMinutes": 539.0,
        "IsWearPeriod": false,
        "StartDateTime": "2009-10-08T21:54:00",
        "StopDateTime": "2009-10-09T06:53:00"
      },
      {
        "CalendarDays": 10,
        "LengthInMinutes": 13707.0,
        "IsWearPeriod": true,
        "StartDateTime": "2009-10-09T06:53:00",
        "StopDateTime": "2009-10-18T19:20:00"
      },
      {
        "CalendarDays": 2,
        "LengthInMinutes": 729.0,
        "IsWearPeriod": false,
        "StartDateTime": "2009-10-18T19:20:00",
        "StopDateTime": "2009-10-19T07:29:00"
      },
      {
        "CalendarDays": 2,
        "LengthInMinutes": 1314.0,
        "IsWearPeriod": true,
        "StartDateTime": "2009-10-19T07:29:00",
        "StopDateTime": "2009-10-20T05:23:00"
      }
    ],
    "DayStats": [
      {
        "Date": "2009-10-05T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 1243875.08,
        "WearTimeInMinutes": 780.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-06T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2223773.66,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-07T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2470233.1,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-08T00:00:00",
        "NonWearTimeInMinutes": 126.0,
        "NonWearTimePercentage": 8.75,
        "VectorMagnitudeCounts": 2259798.37,
        "WearTimeInMinutes": 1314.0,
        "WearTimePercentage": 91.25
      },
      {
        "Date": "2009-10-09T00:00:00",
        "NonWearTimeInMinutes": 413.0,
        "NonWearTimePercentage": 28.68,
        "VectorMagnitudeCounts": 2059471.91,
        "WearTimeInMinutes": 1027.0,
        "WearTimePercentage": 71.32
      },
      {
        "Date": "2009-10-10T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2434605.27,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-11T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2206379.77,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-12T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 1998994.09,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-13T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2489578.45,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-14T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2505689.35,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-15T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2348089.86,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-16T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 2361062.51,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-17T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 1740830.61,
        "WearTimeInMinutes": 1440.0,
        "WearTimePercentage": 100.0
      },
      {
        "Date": "2009-10-18T00:00:00",
        "NonWearTimeInMinutes": 280.0,
        "NonWearTimePercentage": 19.44,
        "VectorMagnitudeCounts": 2327213.44,
        "WearTimeInMinutes": 1160.0,
        "WearTimePercentage": 80.56
      },
      {
        "Date": "2009-10-19T00:00:00",
        "NonWearTimeInMinutes": 449.0,
        "NonWearTimePercentage": 31.18,
        "VectorMagnitudeCounts": 2016794.83,
        "WearTimeInMinutes": 991.0,
        "WearTimePercentage": 68.82
      },
      {
        "Date": "2009-10-20T00:00:00",
        "NonWearTimeInMinutes": 0.0,
        "NonWearTimePercentage": 0.0,
        "VectorMagnitudeCounts": 51534.36,
        "WearTimeInMinutes": 323.0,
        "WearTimePercentage": 100.0
      }
    ]
  }
}
```
