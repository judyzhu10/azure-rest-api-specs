# MySql

> see https://aka.ms/autorest

This is the AutoRest configuration file for MySql.

---

## Getting Started

To build the SDK for MySql, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`

---

## Configuration

### Basic Information

These are the global settings for the MySql API.

``` yaml $(package-singleservers)
tag: package-2020-01-01
```

### Tag: package-2017-12-01-preview

These settings apply only when `--tag=package-2017-12-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2017-12-01-preview'
input-file:
- Microsoft.DBforMySQL/legacy/preview/2017-12-01-preview/mysql.json
```

### Tag: package-2017-12-01

These settings apply only when `--tag=package-2017-12-01` is specified on the command line.

``` yaml $(tag) == 'package-2017-12-01'
input-file:
- Microsoft.DBforMySQL/legacy/stable/2017-12-01/mysql.json
- Microsoft.DBforMySQL/legacy/stable/2017-12-01/ServerSecurityAlertPolicies.json
```

### Tag: package-2018-06-01-privatepreview

These settings apply only when `--tag=package-2018-06-01-privatepreview` is specified on the command line.

``` yaml $(tag) == 'package-2018-06-01-privatepreview'
input-file:
- Microsoft.DBforMySQL/legacy/preview/2018-06-01-privatepreview/mysql.json
- Microsoft.DBforMySQL/legacy/preview/2018-06-01-privatepreview/PrivateEndpointConnections.json
- Microsoft.DBforMySQL/legacy/preview/2018-06-01-privatepreview/PrivateLinkResources.json
```

### Tag: package-2018-06-01

These settings apply only when `--tag=package-2018-06-01` is specified on the command line.

``` yaml $(tag) == 'package-2018-06-01'
input-file:
- Microsoft.DBforMySQL/legacy/stable/2017-12-01/mysql.json
- Microsoft.DBforMySQL/legacy/stable/2017-12-01/ServerSecurityAlertPolicies.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/QueryPerformanceInsights.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/PerformanceRecommendations.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/PrivateEndpointConnections.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/PrivateLinkResources.json
```

### Tag: package-2020-01-01-privatepreview

These settings apply only when `--tag=package-2020-01-01-privatepreview` is specified on the command line.

``` yaml $(tag) == 'package-2020-01-01-privatepreview'
input-file:
- Microsoft.DBforMySQL/legacy/preview/2020-01-01-privatepreview/DataEncryptionKeys.json
```

### Tag: package-2020-01-01

These settings apply only when `--tag=package-2020-01-01` is specified on the command line.

``` yaml $(tag) == 'package-2020-01-01'
input-file:
- Microsoft.DBforMySQL/legacy/stable/2017-12-01/mysql.json
- Microsoft.DBforMySQL/legacy/stable/2017-12-01/ServerSecurityAlertPolicies.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/QueryPerformanceInsights.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/PerformanceRecommendations.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/PrivateEndpointConnections.json
- Microsoft.DBforMySQL/legacy/stable/2018-06-01/PrivateLinkResources.json
- Microsoft.DBforMySQL/legacy/stable/2020-01-01/DataEncryptionKeys.json
- Microsoft.DBforMySQL/legacy/stable/2020-01-01/Servers.json
```

### Tag: package-2020-07-01-privatepreview

These settings apply only when `--tag=package-2020-07-01-privatepreview` is specified on the command line.

``` yaml $(tag) == 'package-2020-07-01-privatepreview'
input-file:
- Microsoft.DBforMySQL/legacy/preview/2020-07-01-privatepreview/mysql.json
```

### Tag: package-2020-07-01-preview

These settings apply only when `--tag=package-2020-07-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2020-07-01-preview'
input-file:
- Microsoft.DBforMySQL/legacy/preview/2020-07-01-preview/mysql.json
```

### Tag: package-flexibleserver-2021-05-01-preview

These settings apply only when `--tag=package-flexibleserver-2021-05-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2021-05-01-preview'
input-file:
- Microsoft.DBforMySQL/legacy/preview/2021-05-01-preview/mysql.json
```

### Tag: package-flexibleserver-2021-05-01

These settings apply only when `--tag=package-flexibleserver-2021-05-01` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2021-05-01'
input-file:
- Microsoft.DBforMySQL/legacy/stable/2021-05-01/mysql.json
```

## Suppression

``` yaml
directive:
  - suppress: PathResourceProviderNamePascalCase
    reason: The name of the provider is Microsoft.DBforMySQL
  - suppress: OperationsApiResponseSchema
    from: mysql.json
    reason: Property isDataAction is not included in get operation reponse body
  - suppress: OperationsApiResponseSchema
    from: Microsoft.DBforMySQL/preview/2021-12-01-preview/ServiceOperations.json
    reason: Property isDataAction is not included in get operation reponse body
```