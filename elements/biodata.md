## BioData

Identifies and describes the subject wearing a device.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>SubjectName</td>
    <td>Identifier for the subject wearing the monitor.
        <p>Restrictions:</p>
        <ul>
            <li>NEO or later: 255 characters</li>
            <li>Pre-NEO: 16 characters</li>
        </ul>
    </td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Sex</td>
    <td><p>Accepted values:</p>
        <ul>
            <li>"Male"</li>
            <li>"Female"</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Height</td>
    <td>Height of the subject.
        <p>Notes:</p>
        <ul>
            <li>The unit of measure (English/Metric) corresponds with the ActiLife setting.</li>
        </ul>
        <p>Restrictions:</p>
        <ul>
            <li>0-500 in</li>
            <li>or 0-500 cm</li>
        </ul>
    </td>
    <td>No</td>
    <td>float</td>
  </tr>
  <tr>
    <td>Weight</td>
    <td>Weight of the subject.
        <p>Notes:</p>
        <ul>
            <li>The  unit of measure (English/Metric) corresponds with the ActiLife setting.</li>
        </ul>
        <p>Restrictions:</p>
        <ul>
            <li>0-2000 lbs</li>
            <li>or 0-2000 kg</li>
        </ul>
    </td>
    <td>No</td>
    <td>float</td>
  </tr>
  <tr>
    <td>Age</td>
    <td>Age of subject.</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Race</td>
    <td>Race of the subject.
        <p>Accepted values:</p>
        <ul>
            <li>"Asian / Pacific Islander"</li>
            <li>"Black / African American"</li>
            <li>"White / Caucasian"</li>
            <li>"Latino / Hispanic"</li>
            <li>"Other"</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>DateOfBirth</td>
    <td></td>
    <td>No</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>Limb</td>
    <td>Limb the device was used.
        <p>Accepted values:</p>
        <ul>
            <li>"Wrist"</li>
            <li>"Waist"</li>
            <li>"Ankle"</li>
            <li>"Upper Arm"</li>
            <li>"Thigh"</li>
            <li>"Chest"</li>
            <li>"Back"</li>
            <li>"Other"</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Side</td>
    <td>Side that the device was used.
        <p>Accepted values:</p>
        <ul>
            <li>"Right"</li>
            <li>"Left"</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Dominance</td>
    <td>Dominance of wear position.
        <p>Accepted values:</p>
        <ul>
            <li>"Dominant"</li>
            <li>"Non-Dominant"</li>
        </ul>
    </td>
    <td>No</td>
    <td>string</td>
  </tr>
</table>
