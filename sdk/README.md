# lusid-drive-sdk
FINBOURNE Technology

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 0.1.185
- Package version: 0.1.185
- Build package: org.openapitools.codegen.languages.PythonClientCodegen
For more information, please visit [https://www.finbourne.com](https://www.finbourne.com)

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import lusid_drive 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import lusid_drive
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import lusid_drive
from lusid_drive.rest import ApiException
from pprint import pprint

configuration = lusid_drive.Configuration()
# Configure OAuth2 access token for authorization: oauth2
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# Defining host is optional and default to https://fbn-ci.lusid.com/drive
configuration.host = "https://fbn-ci.lusid.com/drive"
# Create an instance of the API class
api_instance = lusid_drive.ApplicationMetadataApi(lusid_drive.ApiClient(configuration))

try:
    # [EARLY ACCESS] Get resources available for access control
    api_response = api_instance.list_access_controlled_resources()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ApplicationMetadataApi->list_access_controlled_resources: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://fbn-ci.lusid.com/drive*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ApplicationMetadataApi* | [**list_access_controlled_resources**](docs/ApplicationMetadataApi.md#list_access_controlled_resources) | **GET** /api/metadata/access/resources | [EARLY ACCESS] Get resources available for access control


## Documentation For Models

 - [AccessControlledAction](docs/AccessControlledAction.md)
 - [AccessControlledResource](docs/AccessControlledResource.md)
 - [ActionId](docs/ActionId.md)
 - [IdSelectorDefinition](docs/IdSelectorDefinition.md)
 - [IdentifierPartSchema](docs/IdentifierPartSchema.md)
 - [Link](docs/Link.md)
 - [LusidProblemDetails](docs/LusidProblemDetails.md)
 - [ResourceListOfAccessControlledResource](docs/ResourceListOfAccessControlledResource.md)


## Documentation For Authorization


## oauth2

- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: https://lusid.okta.com/oauth2/default/v1/authorize
- **Scopes**: N/A


## Author

info@finbourne.com


