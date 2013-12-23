# Technical Information

ActiLife will listen on a named pipe (a "socket" that recognizes commands on a specific "server name") to action requests sent in by external programs.  ActiLife will use the same named pipe to respond to action requests.  Any technology that supports reading and writing to and from named pipes will be supported including but not limited to C#, Java, C, C++, Python, Perl, and PHP.

## Encoding and Formatting

All action requests and responses will be marked up using [JSON](http://tools.ietf.org/html/rfc4627) since it is widely supported and can be manually generated and parsed without a library.  Although, many libraries do exist and are recommended.  Encoding will be [UTF-8](http://www.ietf.org/rfc/rfc2279) for actions and responses.

**Notes:**

* Requests should be written in one write to the pipe to allow ActiLife to detect the end of the request.
* Responses will be terminated with "\r\n" to designate the end.
* Although the document is written in Pascal-casing the API supports case-insensitive keywords. Responses should also be parsed with case insensitivity.

## Units of Measurement

The ActiLife API respects the "Unit of Measurement" settings of ActiLife.  Changing this to English or Metric will change the data returned from the API respectively.

## Date Formatting

**Prior to API Version 1.6:**

* DateTime arguments also need to match the region/culture setting on the computer that ActiLife is installed on. For example, 1/30/12 is suitable for EN-US but not for EN-GB as the MM/DD formats are switched for the two languages.

**As of API Version 1.6 and on:**

* DateTime arguments (and response values) must adhere to ISO 8601 format standards and will be in UTC.
* DateTime responses (from ActiLife) will adhere to ISO 8601 format standards and will be in UTC.

## Default Device States

This table describes the states of devices as shipped from ActiGraph.

<table>
  <tr>
    <th>Device</th>
    <th>Subject Name</th>
    <th>Status</th>
  </tr>
  <tr>
    <td>Cletus</td>
    <td>empty</td>
    <td>Reset</td>
  </tr>
  <tr>
    <td>Neo</td>
    <td>"Not Initialized"</td>
    <td>Reset</td>
  </tr>
  <tr>
    <td>GT3X-E</td>
    <td>"Not Initialized"</td>
    <td>Halt</td>
  </tr>
</table>