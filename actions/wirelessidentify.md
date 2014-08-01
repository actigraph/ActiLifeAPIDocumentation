# WirelessIdentify   [API 1.0]

Identifies an ANT device by flashing the LEDs.

**Notes:**

* Wireless scanning must have been started previously.

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
    "Action": "WirelessIdentify",
    "Args": {
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
    "Response": "WirelessIdentify",
    "Success": true,
    "Error": "",
    "Args": { ... }
}
```