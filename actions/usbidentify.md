# USBIdentify [API 1.5]

Identifies a device by flashing the LEDs.

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
</table>

### Example Action

    {
        "Action": "USBIdentify",
        "Args": {
            "Serial": "CLE0123456789"
        }
    }

## Response

### Example Response

    {
        "Response": "USBIdentify",
        "Success": true,
        "Error": "",
        "Args": { ... }
    }