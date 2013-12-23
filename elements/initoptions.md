## InitOptions

Configures a device when initializing.

<table>
  <tr>
    <td>ARGUMENT</td>
    <td>REQUIRED</td>
    <td>TYPE</td>
  </tr>
  <tr>
    <td>SubjectName
Caller defined (no restrictions on value).

Notes:
Max length of 255 characters for GT3X+ devices or newer.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>StartDateTime
Start time for the device to start recording.</td>
    <td>No</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>StopDateTime
Stop time for the device to stop recording.  Can be omitted to allow the device to continue recording indefinitely.</td>
    <td>No</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>SampleRate
Sample rate to use.  Can be Hz value or epoch length in seconds.

Notes:
This depends on ability of device. Older devices are unable to handle multiple samples per second and use an epoch of the seconds.
Accepted Hz values:
30 (default)
40
50
60
70
80
90
100</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Axis
Amount of axis to enable while recording.  This is device dependant (GT3X+ and newer default to 3).

Accepted values:
1
2
3</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Steps
Whether to record steps during recording.

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Inclinometer
Whether to record inclinometer changes during recording.

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>FlashLEDWhileActive
Whether to flash the LED while recording data.

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>FlashLEDInDelay
Whether to flash the LED while in DELAY mode.

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>HeartRate
Whether to record Heart Rate data.

Notes:
Only available on devices capable of using Polar strap or wireless devices.  Must be used with a heart rate strap!
Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Lux
Whether to record ambient light changes during recording.

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>DisableSleepMode
Whether to prevent the device from entering a sleep mode during inactivity.

Notes:
This dramatically reduces battery life!
Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>AntWireless
Enable ANT Wireless capabilities.

Notes:
Only available on w-Devices such as wGT3X+ and wActiSleep+.
Ignored by WirelessInitialize action.
Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>DataSummary
Enable Data Summary capabilities (stores daily summary data into expenditure ‘buckets’).

Notes:
Only available on w-Devices such as wGT3X+ and wActiSleep+.
Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>DoNotUpgradeFW
Prevent FW upgrading during initialization.</td>
    <td>No</td>
    <td>bool</td>
  </tr>
</table>