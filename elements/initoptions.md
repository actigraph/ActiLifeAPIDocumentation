## InitOptions

Configures a device when initializing.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>SubjectName</td>
    <td>Caller defined (no restrictions on value).
        <p>Notes:</p>
        <ul>
            <li>Max length of 255 characters for GT3X+ devices or newer.</li>
        </ul>
    </td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>StartDateTime</td>
    <td>Start time for the device to start recording.</td>
    <td>No</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>StopDateTime</td>
    <td>Stop time for the device to stop recording.  Can be omitted to allow the device to continue recording indefinitely.</td>
    <td>No</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>SampleRate</td>
    <td>Sample rate to use.  Can be Hz value or epoch length in seconds.
        <p>Notes:</p>
        <ul>
            <li>This depends on ability of device. Older devices are unable to handle multiple samples per second and use an epoch of the seconds.</li>
        </ul>
        <p>Accepted Hz values:</p>
        <ul>
            <li>30 (default)</li>
            <li>40</li>
            <li>50</li>
            <li>60</li>
            <li>70</li>
            <li>80</li>
            <li>90</li>
            <li>100</li>
        </ul>
    </td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Axis</td>
    <td>Amount of axis to enable while recording.  This is device dependant (GT3X+ and newer default to 3).
        <p>Accepted values:</p>
        <ul>
            <li>1</li>
            <li>2</li>
            <li>3</li>
        </ul>
    </td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Steps</td>
    <td>Whether to record steps during recording.
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Inclinometer</td>
    <td>Whether to record inclinometer changes during recording.
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>FlashLEDWhileActive</td>
    <td>Whether to flash the LED while recording data.
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>FlashLEDInDelay</td>
    <td>Whether to flash the LED while in DELAY mode.
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>HeartRate</td>
    <td<Whether to record Heart Rate data.
        <p>Notes:</p>
        <ul>
            <li>Only available on devices capable of using Polar strap or wireless devices.  Must be used with a heart rate strap!</li>
        </ul>
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Lux</td>
    <td>Whether to record ambient light changes during recording.
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>DisableSleepMode</td>
    <td>Whether to prevent the device from entering a sleep mode during inactivity.
        <p>Notes:</p>
        <ul>
            <li>This dramatically reduces battery life!</li>
        </ul>
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>AntWireless</td>
    <td>Enable ANT Wireless capabilities.
        <p>Notes:</p>
        <ul>
            <li>Only available on w-Devices such as wGT3X+ and wActiSleep+.</li>
            <li>Ignored by WirelessInitialize action.</li>
        </ul>
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>DataSummary</td> 
    <td>Enable Data Summary capabilities (stores daily summary data into expenditure ‘buckets’).
        <p>Notes:</p>
        <ul>
            <li>Only available on w-Devices such as wGT3X+ and wActiSleep+.</li>
        </ul>
        <p>Accepted values:</p>
        <ul>
            <li>false (default)</li>
            <li>true</li>
        </ul>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>DoNotUpgradeFW</td>
    <td>Prevent FW upgrading during initialization.</td>
    <td>No</td>
    <td>bool</td>
  </tr>
</table>
