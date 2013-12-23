## AGDOptions

Describes what data should be included in the downloaded AGD file.

<table>
  <tr>
    <td>ARGUMENT</td>
    <td>REQUIRED</td>
    <td>TYPE</td>
  </tr>
  <tr>
    <td>Axis
Number of axis to include in AGD. Must be at least 1 Axis to create an AGD!</td>
    <td>Yes</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Steps
Whether to include steps in the AGD (if device was recording steps).

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Lux
Whether to include LUX in the AGD (if device was recording LUX).

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>HR
Whether to include Heart Rate in the AGD (if device was recording Heart Rate).

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Inclinometer
Whether to include Inclinometer data in the AGD (if device was recording inclinometer).

Accepted values:
false (default)
true</td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>EpochLengthInSeconds
Duration of an epoch in seconds.

Accepted values:
1
2
3
5
10
15
30
60
120
150
180
240</td>
    <td>Yes</td>
    <td>int</td>
  </tr>
</table>