# Physical-StreamReaches/doc #

This folder contains files for the ***Physical - Stream Reaches*** product.

* [Introduction](#introduction)
* [Update Frequency](#update-frequency)
* [Datasets](#datasets)
* [Files](#files)
* [Workflow](#workflow)

-----------------------------

## Introduction ##

The ***Physical - Stream Reaches*** map illustrates the locations of streams in the basin,
as lines that generally follow the river/stream center line.
The stream reaches layer is a foundational layer that is displayed on many maps.

## Update Frequency ##

This product is updated infrequently,
based on changes in CDSS Source Water Route Framework dataset.

## Datasets ##

The following are datasets for the map.

| **Dataset** | **Description** | **Data Source** |
| -- | -- | -- |
| Source Water Route Framework (SWRF) | Stream linework with each stream corresponding to a single line.  CO DWR processed USGS NHD layer to merge linework into lines that correspond to rivers and streams. | The data is originally from a statewide layer downloaded from the [State of Colorado CDSS website](https://www.colorado.gov/pacific/cdss/gis-data-category).  It was then processed by OWF to split into water district layer and is available on the [CDSS Spatial Datasets for Colorado Water Districts and Divisions](http://data.openwaterfoundation.org/co/cdss-data-spatial-bybasin/) website.  **The OWF dataset is older and uses the original GeoJSON specification.  The workflow reads the old GeoJSON and writes in latest specification.** |

## Files ##

The following files and folders are used.

| **File/Folder** | **Description** | **Repo Ignore** |
| -- | -- | -- |
| `.gitignore` | Indicates which files should be ignored in the repository. | |
| `01a-download-swrf.gp` | GeoProcessor command file to download data. | |
| `03-create-stream-reaches-map.gp` | GeoProcessor command file to create map. | |
| `doc/` | This `README.md` and related files. | |
| `downloads/` | Downloaded files. | Yes - for downloaded files. |
| `layers/` | Layers and supporting files used in the map. | Yes - for generated files. |
| `stream-reaches.json` | Map configuration file. | Yes |

## Workflow ##

The following describes the workflow steps, which should be run in the order shown to fully regenerate the information products.

| **Command File/Script** | **Software** | **Description** |
| -- | -- | -- |
| `01a-download-swrf.gp` | GeoProcessor | Download the stream reaches from OWF data website and rewrite to ensure latest GeoJSON format. |
| `03-create-stream-reaches-map.gp` | GeoProcessor | Create the map configuration file and copy map and layer files to the distribution folder. |
