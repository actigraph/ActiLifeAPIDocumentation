## AGDOptions

Describes what data should be included in the downloaded AGD file.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Axis</td>
    <td>Number of axis to include in AGD. Must be at least 1 Axis to create an AGD!</td>
    <td>Yes</td>
    <td>int</td>
  </tr>
  <tr>
    <td>Steps</td>
    <td>Whether to include steps in the AGD (if device was recording steps).
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
    <td>Whether to include LUX in the AGD (if device was recording LUX).
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
    <td>HR</td>
    <td>Whether to include Heart Rate in the AGD (if device was recording Heart Rate).
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
    <td>Inclinometer</td>
    <td>Whether to include Inclinometer data in the AGD (if device was recording inclinometer).
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
    <td>EpochLengthInSeconds</td>
    <td>Duration of an epoch in seconds.
        <p>Accepted values:</p>
        <ul>
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>5</li>
            <li>10</li>
            <li>15</li>
            <li>30</li>
            <li>60</li>
            <li>120</li>
            <li>150</li>
            <li>180</li>
            <li>240</li>
        </ul>
    </td>
    <td>Yes</td>
    <td>int</td>
  </tr>
</table>
