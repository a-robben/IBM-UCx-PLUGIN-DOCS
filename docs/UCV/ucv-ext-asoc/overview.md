
HCL AppScan on Cloud (ASoC) - Overview
======================================

# Overview


### Overview



The AppScan on Cloud plug-in allows for integration with the HCL Application Security on Cloud
server. This plug-in uses the Application Security on Cloud REST interface to interact with the HCL Application Security
on Cloud application. Data is gathered from the Application Security on Cloud server and displayed as a graphical view
in the UrbanCode Velocity portfolio.

Compatibility
-------------

Must be running UrbanCode Velocity version 1.2.1
and later to use this plug-in.

Versions
--------

UrbanCode Velocity plug-in images are located in DockerHub. To view
available versions, see the [UrbanCode DockerHub](https://hub.docker.com/r/urbancode/ucv-ext-asoc/tags).

History

-------

### Version 3.0.5

* User access key related changes.

### Version 2.0.1

* Syncs historic data from ASoC.
Also webhook support enabled. Note: This is a **breaking change** as the end point changes from ‘POST’ to ‘GET’

###
Version 1.0.24

* Proxy support added.

### Version 1.0.18

* Bug fix.

### Version 1.0.17

* Added Build URL to
link ASoC scan results in VSM.

### Version 1.0.16

* Bug fixes.

### Version 1.0.14

* Name field in Insights
mapped to the scan name in ASoC.

### Version 1.0.13

* Bug fixes.

### Version 1.0.9

* Update plugin version from
0.x.x to 1.x.x format.

### Version 0.0.4

* Initial release


|Back to ...||Latest Version|HCL AppScan on Cloud (ASoC) |||
| :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Velocity Plugins](../README.md)|[3.0.5](https://raw.githubusercontent.com/UrbanCode/IBM-UCV-PLUGINS/main/files/ucv-ext-asoc/ucv-ext-asoc-3.0.5.tar.zip)|[Readme](README.md)|[Usage](usage.md)|[Downloads](downloads.md)|
