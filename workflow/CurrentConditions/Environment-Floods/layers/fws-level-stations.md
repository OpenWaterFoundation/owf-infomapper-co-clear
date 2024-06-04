# Layer: Flood Warning Water Level Stations #

The Flood Warning System (FWS) water level stations layer contains flood warning water level (stage) stations
for the Greater Denver region,
used to display basic current conditions information and provide links to the FWS station dashboards.

Characteristics of water level stations are as follows:

*   return water level data types
*   are located near a stream or other water body
*   may also collect other data types such as precipitation
*   typically use a pressure transducer or radar below bridges
*   may be taken out of service in cold weather to protect the sensors from freezing

The map marker is currently not color-coded.
The [Mile High Flood District Flood Warning System](https://mhfd-ns5data.trilynx-novastar.systems/novastar/operator/)
provides features to view data and alarm conditions,
including precipitation alarms based on precipitation duration frequency levels (i.e., 10-year storm).

## Data Sources ##

The following are data sources for this map:

| **Resource** | **Source** |
| -- | -- |
| Flood Warning Precipitation Stations | Mile High Flood District FWS data web services. |

## Workflow ##

The workflow to create the map can be found in the
[GitHub repository](https://github.com/OpenWaterFoundation/owf-infomapper-co-clear/tree/master/workflow/CurrentConditions/Environment-Floods).
