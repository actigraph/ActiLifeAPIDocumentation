## BatchExportSheetOptions [API 1.12]

Options for what the data scoring export sheets will contain.

<table>
  <tr>
    <th>Argument</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>AddDefinitionComments</td>
    <td>If enabled and export type is Excel, definition comments will be added to column headers.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>AddDefinitionWorksheet</td>
    <td>If enabled a sheet will be created with definitions of the columns.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>AddWtv</td>
    <td>If enabled a sheet will be created with wear time validation periods for each file.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShowNonWear</td>
    <td>If enabled non-wear times will be included in the export.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShowSummary</td>
    <td>If enabled a sheet will be created with summary results for each file.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShowDaily</td>
    <td>If enabled a sheet will be created with daily results for each file.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShowHourly</td>
    <td>If enabled a sheet will be created with hourly results for each file.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>AddSleepScores</td>
    <td>If enabled a sheet will be created with sleep scores for each file. Sleep scores must be calculated prior to exporting.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShowBoutDetails</td>
    <td>If enabled a sheet will be created with a list of bouts for each file. Bouts must be calculated to included.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>ShowSedentaryDetails</td>
    <td>If enabled a sheet will be created with a list of sedentary bouts for each file. Sedentary bouts must be calculated to included.
        <p>Accepted Values:</p>
        <ul><li>true</li><li>false (default)</ul></td>
    </td>
    <td>No</td>
    <td>bool</td>
  </tr>
</table>
