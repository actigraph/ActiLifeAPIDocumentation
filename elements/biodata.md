## BioData

Identifies and describes the subject wearing a device.

<table>
  <tr>
    <td>ARGUMENT</td>
    <td>REQUIRED</td>
    <td>TYPE</td>
  </tr>
  <tr>
    <td>SubjectName
Identifier for the subject wearing the monitor.

Restrictions:
NEO or later: 255 characters
Pre-NEO: 16 characters</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Sex

Accepted values:
"Male"
"Female"</td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Height
Height of the subject.

Notes:
The unit of measure (English/Metric) corresponds with the ActiLife setting.
Restrictions:
0-500 in
or 0-500 cm</td>
    <td>No</td>
    <td>float</td>
  </tr>
  <tr>
    <td>Weight
Weight of the subject.

Notes:
The  unit of measure (English/Metric) corresponds with the ActiLife setting.
Restrictions:
0-2000 lbs
or 0-2000 kg</td>
    <td>No</td>
    <td>float</td>
  </tr>
  <tr>
    <td>Age
Age of subject.</td>
    <td>No</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Race
Race of the subject.

Accepted values:
"Asian / Pacific Islander"
"Black / African American"
"White / Caucasian"
"Latino / Hispanic"
"Other"</td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>DateOfBirth</td>
    <td>No</td>
    <td>DateTime</td>
  </tr>
  <tr>
    <td>Limb
Limb the device was used.

Accepted values:
"Wrist"
"Waist"
"Ankle"
"Upper Arm"
"Thigh"
"Chest"
"Back"
"Other"</td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Side
Side that the device was used.

Accepted values:
"Right"
"Left"</td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Dominance
Dominance of wear position.

Accepted values:
"Dominant"
"Non-Dominant"</td>
    <td>No</td>
    <td>string</td>
  </tr>
</table>