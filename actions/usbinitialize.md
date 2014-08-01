# USBInitialize [API 1.2]

Initializes a device connected via USB to prepare for a new activity monitoring session.

**Notes:**

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
    <td>Serial</td>
    <td>The device serial number to target.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td><a href="../elements/biodata.md">BioData</a></td>
    <td>Bio information is a nested JSON object. The values will be injected into the file as metadata.</td>
    <td>Yes</td>
    <td>JSON</td>
  </tr>
  <tr>
    <td><a href="../elements/initoptions.md">InitOptions</a></td>
    <td>Initialization options are a nested JSON object.  These values control what is enabled on the device after initialization.</td>
    <td>Yes</td>
    <td>JSON</td>
  </tr>
</table>

### Example Action
```JSON
{
    "Action": "USBInitialize",
    "Args": {
        "Serial": "CLE123456789",
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
            "inclinometer": true,
            "FlashLEDWhileActive": false,
            "FlashLEDInDelay": true,
            "HeartRate": false,
            "Lux": true,
            "DisableSleepMode": true,
            "AntWireless": true,
            "DataSummary": true
        }
    }
}
```
## Response

### Example Response
```JSON
{
    "Response": "USBInitialize",
    "Success": true,
    "Error": "",
    "Args": { ... }
}
```