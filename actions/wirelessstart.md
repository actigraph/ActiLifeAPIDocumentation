# WirelessStart [API 1.0]

Starts the wireless scan of devices.

**Notes:**

* Response payload is only set when a device has been detected and will only contain the ANT ID of the device (everything else will be defaulted values). A second response will be sent when the device’s information is known.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>AntPIN [API 1.6]</td>
    <td>Four character ASCII string.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
</table>

### Example Action

    {
        "Action": "WirelessStart"
        "Args": {
            "AntPIN": "1234"
        }
    }

## Response

### Example Response

    {
        "Response": "WirelessStart",
        "Success": true,
        "Error": "",
        "Payload": {
            "AntID": 124,
            "Serial": "CLE123456789",
            "Status": "Active",
            "Subject": "John Smith",
            "Battery": 3.73,
            "CanRealTimeStream": true,
            "CanBurst": true
        },
        "Args": { ... }
    }