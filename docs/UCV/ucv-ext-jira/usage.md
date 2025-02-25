
Jira - Usage
============

# Usage


### Usage



To use the Jira plug-in, the plug-in must be loaded and an instance created before you can configure
the plug-in integration. You define configuration properties in the user interface or in a JSON file.

Integration type

----------------

The Jira plug-in supports scheduled events integration which are listed in the following table.



| Name | Description |
| --- | --- |
| SyncJiraDataEvent | Synchronize data from a Jira server. |

Integration

-----------

There are two methods to integrate the plug-in:

* Using the user interface
* Using a JSON file

The
tables in the Configuration properties topic describe the properties used to define the integration.

### Using the
user interface

1. From the Plugins page, click **Settings** > **Integrations** > **Plugins**.
2. Under the **Action**
column for the plug-in, click **Add Integration**.
3. On the Add Integration page enter values for the fields used to
configure the integration and define communication.
4. Click **Save**.

### Using a JSON file

The JSON file contains
the information for creating a value stream. Within the JSON file is a section for integrations. It is in this section
that plug-in properties can be defined.

1. From a value stream page, download the value stream map. The value stream
map is a JSON file used to define integrations.
2. Edit the JSON file to include the plug-in configuration properties.

3. Save and upload the JSON file. This replaces the current JSON file with the new content.
4. View the new integration
on the Integrations page.

Configuration properties
------------------------

The following tables describe the
properties used to configure the integration. Each table contains the field name when using the user interface and the
property name when using a JSON file.

* The General Configuration Properties table describes configuration properties
used by all plug-in integrations.
* The Jira Configuration Properties table describes the configuration properties that
define the connection and communications with the Jira server. When using the JSON method to integrate the plug-in these
properties are coded within the `properties` configuration property.


| Name | Description | Required |
| --- | ---
| --- |
| image | The version of the plug-in that you want to use. To view available versions, see the [UrbanCode
DockerHub](https://hub.docker.com/r/urbancode/ucv-ext-jira/tags). If a value is not specified, the latest version is
used. | No |
| name | An assigned name to the value stream. | Yes |
| loggingLevel | The level of Log4j messages to log.
Valid values are: all, debug, info, warn, error, fatal, off, and trace. The default is info. | No |
| properties | List
of plug-in configuration properties used to connect and communicate with the Jira server. Enclose the properties within
braces. | Yes |
| tenant\_id | The name of the tenant. | Yes |
| type | Unique identifier assigned to the plug-in. The
value for the Jira plug-in is `ucv-ext-jira` | Yes |


| Name | Type | Description | Required | Property Name |
| ---
| --- | --- | --- | --- |
| Access Token | String | The access token for oauth authentication with the Jira server. | No
| access\_token |
| Access Token Secret | String | The access token secret for oauth authentication with the Jira
server. | No | access\_token\_secret |
| Consumer Key | String | The consumer key for oauth authentication with the Jira
server. | No | consumer\_key |
| Consumer Secret | String | The consumer secret for oauth authentication with the Jira
server. | No | consumer\_key\_secret |
| Password | Secure | Credential to authenticate with the Jira server. | No |
password |
| Projects *(Deprecated)* | Array | A list of Jira project to import data from. | No | jiraProjects |
| Jira
JQL | String | Any valid JQL Query. | Yes | jiraJql |
| Proxy Server | String | The URL of the proxy server including
the port number. | No | proxyServer |
| Proxy User Name | String | The user name used to authenticate with the proxy
server. | No | proxyUsername |
| Proxy Password | String | The password used to authenticate with the proxy server. | No
| proxyPassword |
| URL | String | The base URL of the Jira server. | Yes | baseUrl |
| User Name | String | The user
name used to authenticate with the Jira server. | No | username |

Example
-------

The following example can be used
as a template to include the Jira plug-in integration into the JSON file. Copy and paste the template into the JSON file
and make the appropriate changes.


```

"integrations": [
{
"type": "ucv-ext-jira",
"tenant_id":
"*tenantid*",
"name": "Jira_Plugin ",
"properties": {
"baseUrl": "*jira\_server\_url*",

"username": "*jira\_server\_user\_name*",
"password": "*jira\_server\_password*",

"consumer_key": null,
"consumer_secret": null,
"access_token": null,
"access_token_secret":
null,
"jiraJql":"*project in ("John-Project")*",
"proxyServer": "*proxy\_server\_url*",

"proxyUsername": "*proxy\_server\_user\_name*",
"proxyPassword": "*proxy\_server\_password*"
}``

}``  ]
```



|Back to ...||Latest Version|Jira |||
| :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Velocity Plugins](../README.md)|[2.2.1](https://raw.githubusercontent.com/UrbanCode/IBM-UCV-PLUGINS/main/files/ucv-ext-jira/ucv-ext-jira-2.2.1.tar.zip)|[Readme](README.md)|[Overview](overview.md)|[Downloads](downloads.md)|
