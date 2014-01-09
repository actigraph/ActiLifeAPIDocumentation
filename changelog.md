# Changelog

The following table describes the changes that have been made to this documentation since its original baseline.  This table shall be maintained as long as this documentation is active.

<table>
  <tr>
    <th>___Date___</th>
    <th>Description of Change</th>
    <th>API/AL Version</th>
  </tr>
  <tr>
    <td>2012-10-01</td>
    <td>Initial Release</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-10-02</td>
    <td>Added support for listing USB devices. Tabularized arguments supported for each action. Converted "0" and "1" values to false and true respectively.  Added usb_list support. Alphabetized action listing.</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-10-04</td>
    <td>Added support for downloading USB devices.  Increased amount of data returned by usb_list.</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-10-15</td>
    <td>Added BIO information and AGD options to USB downloading.</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-10-25</td>
    <td>Added support for initializing USB devices.  Added support for initializing Wireless devices.  Added data types for action arguments.  Made action arguments bold.</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-11-02</td>
    <td>Added action examples.</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-11-05</td>
    <td>Added APIVersion action to return current API version.  Added original args to responses. Condensed action and arg names by removing underscores. Pascal cased for easier reading.</td>
    <td></td>
  </tr>
  <tr>
    <td>2012-12-07</td>
    <td>Added TOC. Added USBIdentify action. Removed nested (and duplicated) argument tables. Added more information to overview with regard to AL being installed, subject name max length, units of measurement, and date formats. Changed table font size from 10 to 9. Added Default Device States. Added bio data restrictions.</td>
    <td></td>
  </tr>
  <tr>
    <td>2013-03-27</td>
    <td>Corrected APIVersion response structure. All dates are now ISO 8601 format. Added ActiLifeVersion action to return current ActiLife version. Added more info to USBList return. Added PIN support to wireless actions. Required epoch length when creating AGD vis USB Download. Merged description column for space.</td>
    <td></td>
  </tr>
  <tr>
    <td>2013-04-10</td>
    <td>Added NAHNESWTV action.</td>
    <td></td>
  </tr>
  <tr>
    <td>2013-04-22</td>
    <td>Added NHANESWTV response and Common Responses section.</td>
    <td></td>
  </tr>
  <tr>
    <td>2013-04-24</td>
    <td>Added InitOptions.DoNotUpgradeFW</td>
    <td></td>
  </tr>
  <tr>
    <td>2013-11-18</td>
    <td>Added documentation for existing --hidegui flag to suppress GUI interruptions of API usage.</td>
    <td></td>
  </tr>
  <tr>
    <td>2013-12-23</td>
    <td>Migrated from single Google Drive document to Github repository. Refactored content single page into sections.</td>
    <td></td>
  </tr>
  <tr>
    <td>2014-01-02</td>
    <td>Improved USBList action with ContinueReportingAsync, TotalDeviceCount, and Siblings.</td>
    <td>1.8/6.9.1</td>
  </tr>
  <tr>
    <td>2014-01-08</td>
    <td>Added Raw CSV export option to USBDownload action. Added API/AL column to changelog.</td>
    <td>1.9/6.10</td>
  </tr>
  <tr>
    <td>2014-01-09</td>
    <td>Added ConvertFile action with gt3x to rawcsv support. Removed "Revision" from changelog as "Date" is sufficient.</td>
    <td>1.9/6.10</td>
  </tr>
</table>
