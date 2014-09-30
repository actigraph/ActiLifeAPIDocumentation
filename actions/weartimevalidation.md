# WearTimeValidation [API 1.11]

Calculate wear time validation results for a single AGD file.

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
    <td>Algorithm</td>
    <td>Which wear time validation algorithm to use
        <p>Accepted values:</p>
        <ul>
            <li>Troiano</li>
            <li>Choi</li>
            <li>Daily</li>
		</ul>
    </td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td><a href="../elements/troianoWTVOptions.md">TroianoWTVOptions</a></td>
    <td>Options for calculating Troiano wear time validation results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/choiWTVOptions.md">ChoiWTVOptions</a></td>
    <td>Options for calculating Choi wear time validation results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr> 
  <tr>
    <td><a href="../elements/dailyWTVOptions.md">DailyWTVOptions</a></td>
    <td>Options for calculating ActiGraph Daily wear time validation results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr> 
</table>

### Example Action
```JSON
{
  "Action": "WearTimeValidation",
  "Args": {
    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd",
	"Algorithm": "Choi"
  }
}
```

## Response

### Example Response
```JSON
{
  "Response": "WearTimeValidation",
  "Success": true,
  "Error": "",
  "Args": {
    "FileInputPath": "c:\\users\\john.doe\\Desktop\\file.agd",
    "Algorithm": "Choi"
  },
  "Payload": {
    "filename": "c:\\users\\john.doe\\Desktop\\file.agd",
    "results": [
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
    ]
  }
}
```
