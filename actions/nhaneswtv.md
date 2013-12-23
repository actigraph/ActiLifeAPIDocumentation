# NHANESWTV [API 1.7]

Returns Wear Time Validation information from a .GT3X file or .AGD file.  This is specific for NHANES.  A more robust WTV API action will be added in the future.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Filename</td>
    <td>The file to process. Supports both AGD and GT3X files.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>MinLength</td>
    <td>Minimum length in minutes of a non-wear period.  Defaults to 60.</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>MinCounts</td>
    <td>Counts at and below this number be considered inactivity.  Defaults to 10.</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>DropTime</td>
    <td>Amount of time in minutes allowed above the MinCounts in a non-wear period.  Defaults to 2.</td>
    <td>No</td>
    <td>int</td>
  </tr>
</table>

### Example Action

    {
        "Action": "NHANESWTV",
         "Args":  {
            "Filename": "c:\dataset.agd",
            "MinLength": 60,
            "MinCounts": 10,
            "DropTime": 2
        }
    }

## Response

<table>
  <tr>
    <th>Element</th>
    <th>Description</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>NonWearBouts</td>
    <td>List of non-wear time bouts.</td>
    <td>Array<<a href="../elements/validationbout.md">ValidationBout</a>></td>
  </tr>
  <tr>
    <td>WearBouts</td>
    <td>List of wear time bouts.</td>
    <td>Array<<a href="../elements/validationbout.md">ValidationBout</a>></td>
  </tr>
  <tr>
    <td>NonWearBoutsCount</td>
    <td>Number of non-wear time bouts.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>WearBoutsCount</td>
    <td>Number of wear time bouts.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>NonWearTimeTotalLength</td>
    <td>Total length of non-wear time in minutes.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>WearTimeTotalLength</td>
    <td>Total length of wear time in minutes.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>NonWearTimeAverage</td>
    <td>Average length of non-wear time bout in minutes.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>WearTimeAverage</td>
    <td>Average length of wear time bout in minutes.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>NonWearTimePerDayAverage</td>
    <td>Average time per day of non-wear time in minutes.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>WearTimePerDayAverage</td>
    <td>Average time per day of wear time in minutes.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>NonWearTimePerDayPercentage</td>
    <td>Percentage of non-wear time.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>WearTimePerDayPercentage</td>
    <td>Percentage of wear time.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>VectorMagnitudeAllData</td>
    <td>Vector magnitude of all data.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>DailySummary</td>
    <td>List of the daily summaries.</td>
    <td>Array<<a href="../elements/daywtv.md">DayWTV</a>></td>
  </tr>
</table>