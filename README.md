# ![LOGO](logo.png) Wealthport API **flow**ground Connector

## Description

A generated **flow**ground connector for the Wealthport API API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/wealthport.com/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:44:51+03:00

## API Description

Onedot provides a simple, lightweight and open Web API based on the Open API 2.0 standard (<a href="https://www.openapis.org" target="_blank">https://www.openapis.org</a>). Our APIs offer a variety of operations related to managing Sources, Folders, Orders and Recipes. There are operations to submit and track Jobs, upload and download data files and many more.

## Authorization

Supported authorization schemes:
- API Key- API Key
## Actions

### Retrieve Folders

> Retrieves all Folders in the Data Inventory.

*Tags:* `Folders`

### Create Folder

> Creates the specified Folder in the Data Inventory.

*Tags:* `Folders`

### Delete Folder

> Deletes the specified Folder and all contained Sources from the Data Inventory.

*Tags:* `Folders`

#### Input Parameters
* `id` - _required_ - Folder ID of the Folder to delete, including any Sources contained

### Retrieve Folder

> Retrieves the specified Folder.

*Tags:* `Folders`

#### Input Parameters
* `id` - _required_ - Folder ID of the Folder to retrieve

### Update Folder

> Updates the specified Folder.

*Tags:* `Folders`

#### Input Parameters
* `id` - _required_ - Folder ID of the Folder to update

### Delete Sources

> Deletes all Sources in the specified Folder.

*Tags:* `Folders`

#### Input Parameters
* `id` - _required_ - Folder ID of the Folder to delete all Sources from

### Retrieve Sources

> Retrieves all Sources of the specified Folder.

*Tags:* `Folders`

#### Input Parameters
* `id` - _required_ - Folder ID of the Folder to retrieve its Sources from

### Get Result

> Returns the result of a finished Job.

*Tags:* `Orders`

#### Input Parameters
* `id` - _required_ - Job ID of the job to retrieve its result

### Get Status

> Retrieves the status of a Job.

*Tags:* `Orders`

#### Input Parameters
* `id` - _required_ - Job ID of the job to retrieve its status

### Retrieve Orders

> Retrieves all previously submitted Orders.

*Tags:* `Orders`

### Create Order

> Creates a new Order to be submitted.<p>Orders reference one or more Sources, e.g. uploaded files, as well as one or more Folders (which again can contain Sources).The Recipe describes what to do with the referenced sources and where to publish the processing result to.</p>

*Tags:* `Orders`

### Delete Order

> Deletes the specified Order.

*Tags:* `Orders`

#### Input Parameters
* `id` - _required_ - Order ID of the order to delete

### Retrieve Order

> Retrieves the specified Order.

*Tags:* `Orders`

#### Input Parameters
* `id` - _required_ - Order ID of the order to retrieve

### Update Order

> Updates the specified Order.

*Tags:* `Orders`

#### Input Parameters
* `id` - _required_ - Order ID of the order to update

### Submit Order

> Submits the specified Order for processing and launches a corresponding job.

*Tags:* `Orders`

#### Input Parameters
* `id` - _required_ - Order ID of the order to submit for processing

### Retrieve Recipes

> Retrieves all available Recipes.

*Tags:* `Recipes`

### Retrieve Recipe

> Retrieves the specified Recipe.

*Tags:* `Recipes`

#### Input Parameters
* `id` - _required_ - Recipe ID of the recipe to retrieve

### Retrieve Instructions

> Retrieves the instructions of the specified Recipe.

*Tags:* `Recipes`

#### Input Parameters
* `id` - _required_ - Recipe ID of the recipe whose instructions to retrieve

### Update Instructions

> Updates the instructions of the specified Recipe.

*Tags:* `Recipes`

#### Input Parameters
* `id` - _required_ - Recipe ID of the recipe whose instructions to update

### Retrieve Sources

> Retrieves all Sources stored in the Data Inventory.

*Tags:* `Sources`

### Create Source

> Creates the specified Source.<p>Sources are either uploaded files or a reference to a database. They are referenced in orders to specify which data needs processing.</p><p>Most clients should probably use the Upload File API which implicitly creates a new source on successful file upload.</p>

*Tags:* `Sources`

### Upload File

> Initiates a file upload and returns the URL where to upload the file to.<p>Calling this API generates a secure, unique and time-restricted URL where the file can be uploaded to. The URL is available in the <pre>Location</pre> HTTP header of the response. The temporal validity of the URL is available in the <pre>Cache-Control</pre> HTTP header of the response.Clients may perform a <pre>HTTP PUT</pre> request on the URL to upload the file using a form where a file <pre>sample.csv</pre> is passed as property <pre>file=sample.csv</pre>. For security reasons, clients must pass all HTTP headers as returned by the <pre>X-WP-Upload-Headers</pre> in the response, together with their values. This procedure ensures a secure, encrypted file upload.</p><p>Note that calling this API automatically generates a Source, there is no need to call the Create Source API.</p>

*Tags:* `Sources`

#### Input Parameters
* `name` - _required_ - Name of the source to create. The name must correspond to the exact file name of the file being uploaded.
* `source` - _optional_ - Existing source ID to create a new version from
* `folder` - _optional_ - Folder ID where to upload source to
* `contentType` - _optional_ - MIME type of the source file
* `encoding` - _optional_ - Encoding of the source file

### Delete Source

> Deletes the specified Source.

*Tags:* `Sources`

#### Input Parameters
* `id` - _required_ - Source ID of the Source to delete

### Retrieve Source

> Retrieves the specified Source.

*Tags:* `Sources`

#### Input Parameters
* `id` - _required_ - Source ID of the source to retrieve

### Update Source

> Updates the specified Source.

*Tags:* `Sources`

#### Input Parameters
* `id` - _required_ - Source ID of Source to update

### Download File

> Initiates a file download and returns the URL where to download the file from.<p>Calling this API generates a secure, unique and time-restricted URL where the file can be downloaded from. The URL is available in the <pre>Location</pre> HTTP header of the response. The time restriction of the URL is availablein the <pre>Cache-Control</pre> HTTP header of the response.Clients may perform a <pre>HTTP GET</pre> request on the URL to download the file.</p>

*Tags:* `Sources`

#### Input Parameters
* `id` - _required_ - Source ID of file to download

## License

**flow**ground :- Telekom iPaaS / wealthport-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
