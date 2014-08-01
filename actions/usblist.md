# USBList [API 1.1]

Lists all connected USB devices and continues listing devices as they are plugged in.

**Notes:**

* ActiLife will send one response per device connected.
* **AntID** will only be provided for ANT capable devices.

## Action

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>TYPE</th>
  </tr>
  <tr>
    <td>ContinueReportingAsync [API 1.8]</td>
    <td>Instructs ActiLife to continue notifying when devices are connected.  If disabled, ActiLife will send a response for each device connected and NOT continue to notify when new devices are connected.
        <p>Notes:</p>
        <ul>
            <li>To regain the asynchronous functionality simply issue the USBList action with this turned on.</li>
		</ul>
        <p>Accepted values:</p>
        <ul>
            <li>true (default)</li>
            <li>false</li>
		</ul>
	</td>
    <td>No</td>
    <td>bool</td>
  </tr>
</table>

### Example Action
```JSON
{
    "Action": "USBList"
}
```
## Response

<table>
  <tr>
    <th>Element</th>
    <th>Description</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>AntID</td>
    <td>The ANT ID of the device. Can be used to wirelessly interact with the device if wireless is enabled on the device.</td>
    <td>string</td>
  </tr>
  <tr>
    <td>BatteryVoltage [API 1.6]</td>
    <td>The current battery voltage reported by the device.</td>
    <td>double</td>
  </tr>
  <tr>
    <td>BatteryPercent [API 1.6]</td>
    <td>The current percentage (out of 100%) of the device’s battery.</td>
    <td>float</td>
  </tr>
  <tr>
    <td>Serial</td>
    <td>The serial number of the device. Can be used to interact with a device connected via USB.</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Status</td>
    <td>The current state of the device.
        <p>Possible values:</p>
        <ul>
            <li>"Active"</li>
            <li>"Halt"</li>
            <li>"Delay"</li>
            <li>"Reset"</li>
            <li>"Finished updating"</li>
            <li>"Finished initializing"</li>
        </ul>
    </td>
    <td>string</td>
  </tr>
  <tr>
    <td>Subject</td>
    <td>The "Subject Name"</td>
    <td>string</td>
  </tr>
  <tr>
    <td>StartTime [API 1.6]</td>
    <td>The time the device started recording data. This value is localized to the timezone of the computer that did the initialization.</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>StopTime [API 1.6]</td>
    <td>The time the device stopped recording data. This value is localized to the timezone of the computer that did the initialization.  This value can be NULL.</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>Firmware [API 1.6]</td>
    <td>The version of firmware on the device.</td>
    <td>string</td>
  </tr>
  <tr>
    <td>SampleRate [API 1.6]</td>
    <td>The configured sample rate at which the device collects raw data. This is typically a value between 30 and 100.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>TotalDeviceCount [API 1.8]</td>
    <td>The number of connected devices.</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Siblings [API 1.8]</td>
    <td>A list of other device serial numbers available.</td>
    <td>Array&lt;string&gt;</td>
  </tr>
</table>

### Example Response
```JSON
{
    "Response": "USBList",
    "Success": true,
    "Error": "",
    "Args": { ... },
    "Payload": {
        "AntID": 124,
        "Serial": "CLE123456789",
        "Status": "Active",
        "Subject": "John Smith",
        "BatteryVoltage": 3.92,
        "BatteryPercentage": 99.9,
        "SampleRate": 30,
        "Firmware": "3.0.0",
        "TotalDeviceCount": 3,
        "Siblings": ["CLE2A01234567","CLE2A76543210"]
    }
}
```