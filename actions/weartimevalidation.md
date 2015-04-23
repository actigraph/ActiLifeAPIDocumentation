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
		</ul>
    </td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td><a href="../elements/troianoWTVOptions.md">TroianoOptions</a></td>
    <td>Options for calculating Troiano wear time validation results.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/choiWTVOptions.md">ChoiOptions</a></td>
    <td>Options for calculating Choi wear time validation results.</td>
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

### Default Troiano Options in full JSON form
```json
{  
    "Action":"WearTimeValidation",
    "Args":{  
        "FileInputPath":"c:\\users\\john.doe\\Desktop\\HKAtlanta.agd",
        "Algorithm":"Troiano",
        "TroianoOptions":{  
            "Algorithm":0,
            "MinimumLengthUnits":0,
            "UseActivityThreshold":false,
            "ActivityThreshold":0,
            "ActivityThresholdUnits":0,
            "UseMaxCount":false,
            "MaxCount":0,
            "MaxCountUnits":0,
            "SpikeTolerance":2,
            "SpikeToleranceUnits":0,
            "UseCountsToStopNonWearPeriod":true,
            "CountsToStopNonWearPeriod":100,
            "CountsToStopNonWearPeriodUnits":0,
            "UseConsecutiveEpochs":true,
            "AutoSleepScoringRequireStartEndZeros":false,
            "AutoSleepScoringStartEpochsToBeZero":0,
            "AutoSleepScoringEndpochsToBeZero":0,
            "MinimumLength":60,
            "VM":false,
            "UseIgnoreShortWearPeriods":false,
            "ShortWearPeriodsLength":0,
            "ShortWearPeriodsUnits":0,
            "UseMinimumWearTimePerDay":false,
            "MinimumWearTimePerDayLength":0,
            "MinimumWearTimePerDayUnits":0,
            "MinimumDaysOfValidWearTime":0,            
            "Sleep":0,
            "UseWearSenseData":true
        }
    }
}
```

### Default Choi Options in full JSON form
```json
{  
    "Action":"WearTimeValidation",
    "Args":{  
        "FileInputPath":"c:\\users\\john.doe\\Desktop\\HKAtlanta.agd",
        "Algorithm":"Choi",
        "ChoiOptions":{  
            "Algorithm":1,
            "SmallWindow":30,
            "SpikeTolerance":2,
            "MinimumLength":90,
            "VM":false,
            "UseIgnoreShortWearPeriods":false,
            "ShortWearPeriodsLength":0,
            "ShortWearPeriodsUnits":0,
            "UseMinimumWearTimePerDay":false,
            "MinimumWearTimePerDayLength":0,
            "MinimumWearTimePerDayUnits":0,
            "MinimumDaysOfValidWearTime":0,
            "Sleep":0,
            "UseWearSenseData":true
        }
    }
}
```