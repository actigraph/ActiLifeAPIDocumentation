# WirelessInitialize [API 1.2]

Initializes an ANT device (only available on w-Devices such as wGT3X+ and wActiSleep+).

**Notes:**

* Wireless scanning must have been started previously.
* Will remove all activity data from the device.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>AntID</td>
    <td>The ANT+ identifier for the targeted device.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>TimeoutSeconds</td>
    <td>The timeout in seconds before ActiLife returns a failure because of timeout.</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td><a href="../elements/biodata.md">BioData</a></td>
    <td>Bio information is a nested JSON object. The values will be sent to the device.</td>
    <td>Yes</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/initoptions.md">InitOptions</a></td>
    <td>Initialization options are a nested JSON object. These values control what is enabled on the device after initialization.</td>
    <td>Yes</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td>AntPIN [API 1.6]</td>
    <td>Four character ASCII string.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
</table>

### Example Action
```JSON
{
    "Action": "WirelessInitialize",
    "Args": {
        "AntID": "123",
        "TimeoutSeconds": 30,
        "AntPIN": "1234",
        "BioData": {
            "SubjectName": "John Doe",
            "Sex": "Male",
            "Height": 182.9,
            "Weight": 175.8,
            "Age": 32,
            "Race": "White / Caucasian",
            "DateOfBirth": "1980-01-01T13:00:00Z",
            "Limb": "Waist",
            "Side": "Right",
            "Dominance": "Dominant"
        },
        "InitOptions": {
            "SampleRate": 40,
            "StartDateTime": "2013-03-20T13:15:00Z",
            "Axis": 3,
            "Steps": true,
            "Inclinometer": true,
            "FlashLEDWhileActive": false,
            "FlashLEDInDelay": true,
            "HeartRate": false,
            "Lux": true,
            "DisableSleepMode": true,
            "DataSummary": true
        }
    }
}
```
## Response

### Example Response
```JSON
{
    "Response": "WirelessInitialize",
    "Success": true,
    "Error": "",
    "Args": { ... }
}
```