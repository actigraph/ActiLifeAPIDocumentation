# WirelessRealtimeStart [API 1.0]

Start receiving data real time from an ANT device. Wireless scanning must have been started previously.

**Notes:**

* Wireless scanning must have been started previously.
* Real time streaming data will not arrive if the device isn’t being moved; the data should be considered latched.  If sleep mode is disabled during initialization then continuous data is to be expected.

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
    <td>AntPIN [API 1.6]</td>
    <td>Four character ASCII string.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
</table>

### Example Action
```JSON
{
    "Action": "WirelessRealtimeStart",
    "Args":  {
        "AntID": "123",
        "TimeoutSeconds": 30,
        "AntPIN": "1234"
    }
}
```
## Response

### Example Response
```JSON
{
    "Response": "WirelessRealtimeStart",
    "Success": true,
    "Error": "",
    "Payload": {
        [
            { "Timestamp": "<UTC Timestamp>",
                "Axis": [ <axis1 (Y)>, <axis2 (Z)>, <axis3 (X)> ],
                "HeartRate": <BPM if sensor connected>,
                "Lux": <value from light sensor>
            },
            {...}
        ]
    },
    "Args": { ... }
}
```