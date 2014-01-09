# ActiLife API

* **Document #:** ATL12DOC06
* **Revision:** N [changelog](changelog.md)
* **Revision Date:** 2013-12-23

**Prepared By:**
  
* [Jeremy Moore](https://github.com/jeremydavidmoore) - Software Developer
* [Derek Gates](https://github.com/derekgates) - Software Developer

## Overview

The ActiLife API was developed so that other software products can utilize [ActiGraph monitors](http://www.actigraphcorp.com/product-category/activity-monitors) outside of the [ActiLife](http://www.actigraphcorp.com/product-category/software) software itself.  However, currently ActiLife must be installed on the machine that will communicate with the API.  As with ActiLife, the ActiLife API is only supported in a Windows environment. However, a piece of software can be written that talks to any operating system over any protocol.

[Technical information](technical.md) is also available.

## Enabling the ActiLife API

The ActiLife API is supported as a opt-in feature only.  It does not work with any ActiLife installation.  This feature must be turned on for your product key.  Please contact [ActiGraph](http://www.actigraphcorp.com/support/contact-support/) for more information.

## Actions

Actions are sent to ActiLife to instruct it to either do something or return data.

<table>
  <tr>
    <th>Element</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Action</td>
    <td>The action to be processed.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Args</td>
    <td>Array of nested elements to configure the action.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
</table>

### Example Action

    {
        "Action": "WirelessIdentify",
        "Args": {
            "AntID": 124,
            "TimeoutSeconds": 30
        }
    }


### Available Actions [A-Z]

* [ActiLifeMinimize [API 1.0]](actions/actilifeminimize.md)
* [ActiLifeRestore [API 1.0]](actions/actiliferestore.md)
* [ActiLifeVersion [API 1.6]](actions/actilifeversion.md)
* [APIVersion [API 1.4]](actions/apiversion.md)
* [ConvertFile [API 1.9]](actions/convertfile.md)
* [NHANESWTV [API 1.7]](actions/nhaneswtv.md)
* [USBDownload [API 1.2]](actions/usbdownload.md)
* [USBIdentify [API 1.5]](actions/usbidentify.md)
* [USBInitialize [API 1.2]](actions/usbinitialize.md)
* [USBList [API 1.1]](actions/usblist.md)
* [WirelessBurst [API 1.0]](actions/wirelessburst.md)
* [WirelessIdentify [API 1.0]](actions/wirelessidentify.md)
* [WirelessInitialize [API 1.2]](actions/wirelessinitialize.md)
* [WirelessRealtimeStart [API 1.0]](actions/wirelessrealtimestart.md)
* [WirelessRealtimeStop [API 1.0]](actions/wirelessrealtimestop.md)
* [WirelessStart [API 1.0]](actions/wirelessstart.md)
* [WirelessStop [API 1.0]](actions/wirelessstop.md)

### Common Elements [A-Z]

* [AGDOptions](elements/agdoptions.md)
* [BioData](elements/biodata.md)
* [InitOptions](elements/initoptions.md)

## Responses

Responses sent from ActiLife either describe that the requested action was processed successfully, failed for a given reason, failed for an unknown reason, or provide data as it becomes available to ActiLife.

<table>
  <tr>
    <th>Element</th>
    <th>Description</th>
    <th>Required</th>
    <th>Type</th>
  </tr>
  <tr>
    <td>Response</td>
    <td>The action in which the response pertains to.</td>
    <td>Yes</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Success</td>
    <td>If the action completed without error.</td>
    <td>Yes</td>
    <td>bool</td>
  </tr>
  <tr>
    <td>Error</td>
    <td>What went wrong, if anything. This value is sent with the response if success == false.</td>
    <td>No</td>
    <td>string</td>
  </tr>
  <tr>
    <td>Args</td>
    <td>The original Args sent from the corresponding Action.</td>
    <td>No</td>
    <td>JSON</td>
  </tr>
</table>

### Common Elements [A-Z]

* [BoutData](elements/boutdata.md)
* [DayWTV](elements/daywtv.md)
* [ValidationBout](elements/validationbout.md)

### Error Responses [A-Z]

* [ErrorGeneral](responses/errorgeneral.md)
* [ErrorInvalidSyntax](responses/errorinvalidsyntax.md)
* [ErrorUnknownAction](responses/errorunknownaction.md)

## ActiLife API Flags

You can start ActiLife 6.7.0 or greater with the following flags to configure its behavior when using the API.

<dl>
    <dt>--hidegui</dt>
    <dd>Suppresses messages and notifications from ActiLife.  No GUI will be shown when ActiLife is started with this flag.  Note: This will cause ActiLife to NOT show the upgrade prompt and effectively never be upgraded.</dd>
</dl>
