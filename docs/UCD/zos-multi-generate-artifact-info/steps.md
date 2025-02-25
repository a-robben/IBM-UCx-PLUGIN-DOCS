
z/OS Multi Generate Artifact Information - Steps
================================================

# Steps


### Steps



Process steps in the zOS Multi Generate Artifact Information plug-in
--------------------------------------------------------------------

* [Generate Multiple Artifact Information](#generate_multiple_artifact_information)


Generate Multiple Artifact Information
--------------------------------------

Generate multiple text information for selected version artifacts. The information is sent to the output properties for use by later steps. **Note:** Action filter is applicable only if **Backup** is enabled in **deploy data sets** step


| Name | Type | Description | Required | Property Name |
| --- | --- | --- | --- | --- |
| Container Name Filter JSON | String | The filter to limit Source datasets in template for an output property. Specify the filter as a Java regular expression matching which must begin and end with a forward slash (/). For example, /.\*LOAD/ matches any text that ends with LOAD. If the filter is not a regular expression, exact matching is used. | No | srcDatasetName |
| Custom Properties Filter JSON | String | The filter to limit Custom properties in the template for an output property. Specify each filter in the format: propertyName=valueFilter and separate each filter with a newline character. A property without a value selects all artifacts related to the specified property. Java regular expression matching is used if the filter begins and ends with a forward slash (/). For example, developer=/M.\*/ matches artifacts for the developer property where the value of the property starts with M. | No | custProperties |
| Deploy Type Filter JSON | String | The filter to limit Deploy Types in template for an output property. Specify the filter as a Java regular expression matching which must begin and end with a forward slash (/). For example, specify /.\*SRC.\*/ to match any text that contains SRC. If the filter is not a regular expression, exact matching is used. | No | deployTypeName |
| Deployment action Filter JSON | String | The filter to limit target datasets and members based on type of deployment action performed. Possible action values are ‘created’ or ‘updated’. For example: If the action value is set to ‘created’ then artifacts which are newly created in target environment are selected. Note: Action values are case insensitive. If value is empty or no value is passed then both ‘created’ and ‘updated’ artifacts are selected. | No | deployAction |
| For Each | Enumeration | Generate information for each of the selected artifact type. Valid value types are: PDS, sequential, deleted member, deleted PDS, and deleted sequential. | Yes | loopType |
| Order By | Enumeration | Order by ASC,DESC, or SHIPLIST. | Yes | orderBy |
| Resource Name Filter JSON | String | The filter to limit PDS Members in template for an output property. Specify the filter as a Java regular expression matching which must begin and end with a forward slash(/). For example, /PGM.\*/ matches any text that starts with PGM. If the filter is not a regular expression, exact matching is used. | No | memberName |
| Target Data Set Name Filter JSON | String | The filter to limit Target datasets in template for an output property. Specify the filter as a Java regular expression matching which must begin and end with a forward slash(/). For example, /.\*LOAD/ matches any text that ends with LOAD. If the filter is not a regular expression, exact matching is used. | No | datasetName |
| Template JSON | String | Define template for each output property to generate customized text. Subsequent steps can access the customized text with ``${p:Step-Name/output-property-name}``. For example: if the step name is ‘Bind Card Generator’ and output property is ‘CicsBindText’ then the property can be referred in subsequent steps as ``${p:Bind Card Generator/CicsBindText}``. Add separators like comma or newline using character ‘,’ or ‘\n’ in the template as needed. Use ``${propname}`` to access custom properties. The following built-in properties are available: ``${sourceDataset}`` for the source dataset name, ``${dataset}`` for the target dataset name, ``${member}`` for the member name and ``${deployType}`` for the deployment type. All property names are case-sensitive. Do not use the built-in names for custom properties. | Yes | templateText |





|Back to ...||Latest Version|z/OS Multi Generate Artifact Information ||||
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Deploy Plugins](../README.md)|[6.1132902](https://raw.githubusercontent.com/UrbanCode/IBM-UCD-PLUGINS/main/files/zos-multi-generate-artifact-info/ucd-plugins-zos-multi-generate-artifact-info-6.1132902.zip)|[Readme](README.md)|[Overview](overview.md)|[Usage](usage.md)|[Downloads](downloads.md)|
