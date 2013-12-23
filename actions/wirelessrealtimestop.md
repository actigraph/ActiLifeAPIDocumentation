# WirelessRealtimeStop [API 1.0]

Stop receiving data real time from an ANT device.

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
</table>

### Example Action

    {
        "Action": "WirelessRealtimeStop",
        "Args": {
            "AntID": "123"
        }
    }

## Response

### Example Response

    {
        "Response": "WirelessRealtimeStop",
        "Success": true,
        "Error": "",
        "Args": { ... }
    }