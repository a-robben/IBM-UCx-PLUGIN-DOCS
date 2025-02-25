
z/OS Multi Generate Artifact Information - Overview
===================================================

# Overview


### Overview



The z/OS Multi Generate Artifact Information plug-in scans version artifacts and generates text based on a template. You can use the generated output text as input to subsequent steps. The plug-in processes data sets and members in a component version.

This plug-in is an extension of the z/OS Utility plug-in for generating artifact information. The z/OS Multiple Generate Artifact Information plug-in have additional features given below.

* Ability to set multiple templates to multiple properties
* Ability to generate multiple properties using one step

This plug-in contains one step:

* Generate Multiple Artifact Information

Use the Generate Multiple Artifact Information step to select a set of artifacts to process by applying filters on data set names, member names, deployment types, and custom properties for each output property.

### Compatibility

This plug-in requires UrbanCode Deploy version 6.1.1 or later and an UrbanCode Deploy agent on z/OS.

This plug-in works with IBM z/OS version 1.9 or later.

### Step palette

To access this plug-in in the palette, click **Utilities** > **zOS Multi Generate Artifact Information**.

### Installation

This plug-in is installed when installing IBM UrbanCode Deploy. When new plug-in versions are available, follow the [installation instructions](https://www.urbancode.com/resource/installing-plug-ins-in-urbancode-products/ "Installing plug-ins in UrbanCode Deploy") to update the plug-in.

### History

#### Version 6

* Minor improvemnets in plugin name and description
* PH46505 Fixed issue with filtering containers mapped to same Target PDS in Generate Artifact step

#### Version 5

* Delete and Update/Create Deploy-Action types on same container/PDS is made possible
* Added input to filter based on artifact created or updated

#### Version 4

* Added support to optionally ignore unresolved properties

#### Version 3

* Added support to run in non zOS environment as well

#### Version 1

* Initial release


|Back to ...||Latest Version|z/OS Multi Generate Artifact Information ||||
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Deploy Plugins](../README.md)|[6.1132902](https://raw.githubusercontent.com/UrbanCode/IBM-UCD-PLUGINS/main/files/zos-multi-generate-artifact-info/ucd-plugins-zos-multi-generate-artifact-info-6.1132902.zip)|[Readme](README.md)|[Steps](steps.md)|[Usage](usage.md)|[Downloads](downloads.md)|
