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

``` yaml
title: MySQLManagementClient
description: The Microsoft Azure management API provides create, read, update, and delete functionality for Azure MySQL resources including servers, databases, firewall rules, VNET rules, log files and configurations with new business model.
openapi-type: arm
tag: package-flexibleserver-2024-12-01-preview
```

### Tag: package-flexibleserver-2024-12-01-preview

These settings apply only when `--tag=package-flexibleserver-2024-12-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2024-12-01-preview'
input-file:
- preview/2024-12-01-preview/AzureADAdministrator.json
- preview/2024-12-01-preview/Backups.json
- preview/2024-12-01-preview/BackupAndExport.json
- preview/2024-12-01-preview/LongRunningBackups.json
- preview/2024-12-01-preview/Configurations.json
- preview/2024-12-01-preview/Databases.json
- preview/2024-12-01-preview/FirewallRules.json
- preview/2024-12-01-preview/FlexibleServers.json
- preview/2024-12-01-preview/AdvancedThreatProtectionSettings.json
- preview/2024-12-01-preview/LogFiles.json
- preview/2024-12-01-preview/ServiceOperations.json
- preview/2024-12-01-preview/Maintenances.json
- preview/2024-12-01-preview/PrivateEndpointConnections.json
- preview/2024-12-01-preview/PrivateLinkResources.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
  - code: PatchBodyParametersSchema
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: DeleteResponseCodes
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: LroLocationHeader
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: ProvisioningStateSpecifiedForLROPut
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: ProvisioningStateSpecifiedForLROPatch
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: ResourceNameRestriction
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: PostResponseCodes
    from: FlexibleServers.json
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: GetCollectionOnlyHasValueAndNextLink
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: XmsPageableForListCalls
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: AvoidAdditionalProperties
    from: ServiceOperations.json
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: OperationsApiResponseSchema
    from: ServiceOperations.json
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: OperationsApiSchemaUsesCommonTypes
    from: ServiceOperations.json
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
  - code: RequiredPropertiesMissingInResourceModel
    from: ServiceOperations.json
    reason: "The new version file for 2024-12-01 was fully copied from the last existing file. Some files are too old to pass verification, and modifying them in this change would be too large. With future updates, we will gradually remove those suppressions."
```
### Tag: package-flexibleserver-2021-12-01-preview

These settings apply only when `--tag=package-flexibleserver-2021-12-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2021-12-01-preview'
input-file:
- preview/2021-12-01-preview/Backups.json
- preview/2021-12-01-preview/Configurations.json
- preview/2021-12-01-preview/Databases.json
- preview/2021-12-01-preview/FirewallRules.json
- preview/2021-12-01-preview/FlexibleServers.json
- preview/2021-12-01-preview/LogFiles.json
- preview/2021-12-01-preview/ServiceOperations.json
- preview/2021-12-01-preview/AzureADAdministrator.json
```

### Tag: package-flexibleserver-2022-09-30-preview

These settings apply only when `--tag=package-flexibleserver-2022-09-30-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2022-09-30-preview'
input-file:
- preview/2021-12-01-preview/AzureADAdministrator.json
- preview/2022-09-30-preview/Backups.json
- preview/2022-09-30-preview/BackupAndExport.json
- preview/2021-12-01-preview/Configurations.json
- preview/2021-12-01-preview/Databases.json
- preview/2021-12-01-preview/FirewallRules.json
- preview/2022-09-30-preview/FlexibleServers.json
- preview/2021-12-01-preview/LogFiles.json
- preview/2022-09-30-preview/ServiceOperations.json
- common-types/v1/common-types.json
suppressions:
  - code: PropertiesTypeObjectNoDefinition
    from: common-types.json
    reason: This will be fixed in new versions.
```

### Tag: package-flexibleserver-2023-06-01-preview

These settings apply only when `--tag=package-flexibleserver-2023-06-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-06-01-preview'
input-file:
- preview/2023-06-01-preview/AzureADAdministrator.json
- preview/2023-06-01-preview/Backups.json
- preview/2023-06-01-preview/BackupAndExport.json
- preview/2023-06-01-preview/Configurations.json
- preview/2023-06-01-preview/Databases.json
- preview/2023-06-01-preview/FirewallRules.json
- preview/2023-06-01-preview/FlexibleServers.json
- preview/2023-06-01-preview/LogFiles.json
- preview/2023-06-01-preview/ServiceOperations.json
- common-types/v1/common-types.json //todo
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PropertiesTypeObjectNoDefinition
    from: common-types.json
    reason: This will be fixed in new versions.
```

### Tag: package-flexibleserver-2023-06-01-preview-new

These settings apply only when `--tag=package-flexibleserver-2023-06-01-preview-new` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-06-01-preview-new'
input-file:
- preview/2023-06-01-preview/AzureADAdministrator.json
- preview/2023-06-01-preview/Backups.json
- preview/2023-06-01-preview/BackupAndExport.json
- preview/2023-06-01-preview/Configurations.json
- preview/2023-06-01-preview/Databases.json
- preview/2023-06-01-preview/FirewallRules.json
- preview/2023-06-01-preview/FlexibleServers.json
- preview/2023-06-01-preview/LogFiles.json
- preview/2021-12-01-preview/ServiceOperations.json
- common-types/v1/common-types.json //todo
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PropertiesTypeObjectNoDefinition
    from: common-types.json
    reason: This will be fixed in new versions.
```

### Tag: package-flexibleserver-2023-06-30

These settings apply only when `--tag=package-flexibleserver-2023-06-30` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-06-30'
input-file:
- stable/2023-06-30/AzureADAdministrator.json
- stable/2023-06-30/Backups.json
- stable/2023-06-30/BackupAndExport.json
- stable/2023-06-30/Configurations.json
- stable/2023-06-30/Databases.json
- stable/2023-06-30/FirewallRules.json
- stable/2023-06-30/FlexibleServers.json
- stable/2023-06-30/LogFiles.json
- stable/2023-06-30/ServiceOperations.json
- preview/2023-10-01-preview/Maintenances.json
- common-types/v1/common-types.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PropertiesTypeObjectNoDefinition
    from: common-types.json
    reason: This will be fixed in new versions.
```

### Tag: package-flexibleserver-2023-10-01-preview

These settings apply only when `--tag=package-flexibleserver-2023-10-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-10-01-preview'
input-file:
- preview/2023-06-01-preview/AzureADAdministrator.json
- preview/2023-06-01-preview/Backups.json
- preview/2023-06-01-preview/BackupAndExport.json
- preview/2023-06-01-preview/Configurations.json
- preview/2023-06-01-preview/Databases.json
- preview/2023-06-01-preview/FirewallRules.json
- preview/2023-10-01-preview/FlexibleServers.json
- preview/2023-06-01-preview/LogFiles.json
- preview/2023-06-01-preview/ServiceOperations.json
- preview/2023-10-01-preview/AdvancedThreatProtectionSettings.json
- common-types/v1/common-types.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
```

### Tag: package-flexibleserver-2023-12-01-preview

These settings apply only when `--tag=package-flexibleserver-2023-12-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-12-01-preview'
input-file:
- preview/2023-06-01-preview/AzureADAdministrator.json
- preview/2023-10-01-preview/Backups.json
- preview/2023-10-01-preview/BackupAndExport.json
- preview/2023-10-01-preview/LongRunningBackups.json
- preview/2023-06-01-preview/Configurations.json
- preview/2023-06-01-preview/Databases.json
- preview/2023-06-01-preview/FirewallRules.json
- preview/2023-12-01-preview/FlexibleServers.json
- preview/2023-12-01-preview/AdvancedThreatProtectionSettings.json
- preview/2023-06-01-preview/LogFiles.json
- preview/2023-12-01-preview/ServiceOperations.json
- preview/2023-10-01-preview/Maintenances.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    from: LongRunningBackups.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutResponseCodes
    from: AdvancedThreatProtectionSettings.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
```

### Tag: package-flexibleserver-2023-12-30

These settings apply only when `--tag=package-flexibleserver-2023-12-30` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-12-30'
input-file:
- preview/2023-06-01-preview/AzureADAdministrator.json
- preview/2023-10-01-preview/Backups.json
- preview/2023-10-01-preview/BackupAndExport.json
- preview/2023-10-01-preview/LongRunningBackups.json
- preview/2023-06-01-preview/Configurations.json
- preview/2023-06-01-preview/Databases.json
- preview/2023-06-01-preview/FirewallRules.json
- stable/2023-12-30/FlexibleServers.json
- stable/2023-12-30/AdvancedThreatProtectionSettings.json
- preview/2023-06-01-preview/LogFiles.json
- stable/2023-12-30/ServiceOperations.json
- preview/2023-10-01-preview/Maintenances.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    from: LongRunningBackups.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutResponseCodes
    from: AdvancedThreatProtectionSettings.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
```

### Tag: package-flexibleserver-2024-01-01

These settings apply only when `--tag=package-flexibleserver-2024-01-01` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2024-01-01'
input-file:
- stable/2023-12-30/AzureADAdministrator.json
- stable/2023-12-30/Backups.json
- stable/2023-12-30/BackupAndExport.json
- stable/2023-12-30/LongRunningBackups.json
- stable/2023-12-30/Configurations.json
- stable/2023-12-30/Databases.json
- stable/2023-12-30/FirewallRules.json
- stable/2023-12-30/FlexibleServers.json
- stable/2023-12-30/AdvancedThreatProtectionSettings.json
- stable/2023-12-30/LogFiles.json
- stable/2023-12-30/ServiceOperations.json
- stable/2023-12-30/Maintenances.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    from: LongRunningBackups.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutResponseCodes
    from: AdvancedThreatProtectionSettings.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
```

### Tag: package-flexibleserver-2024-02-01-preview

These settings apply only when `--tag=package-flexibleserver-2024-02-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2024-02-01-preview'
input-file:
- stable/2023-12-30/AzureADAdministrator.json
- stable/2023-12-30/Backups.json
- stable/2023-12-30/BackupAndExport.json
- stable/2023-12-30/LongRunningBackups.json
- stable/2023-12-30/Configurations.json
- stable/2023-12-30/Databases.json
- stable/2023-12-30/FirewallRules.json
- stable/2023-12-30/LogFiles.json
- stable/2023-12-30/ServiceOperations.json
- stable/2023-12-30/Maintenances.json
- preview/2024-02-01-preview/FlexibleServers.json
- preview/2024-02-01-preview/AdvancedThreatProtectionSettings.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    from: LongRunningBackups.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutResponseCodes
    from: AdvancedThreatProtectionSettings.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
```

### Tag: package-flexibleserver-2024-06-01-preview

These settings apply only when `--tag=package-flexibleserver-2024-06-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2024-06-01-preview'
input-file:
- stable/2023-12-30/AzureADAdministrator.json
- stable/2023-12-30/Backups.json
- stable/2023-12-30/BackupAndExport.json
- stable/2023-12-30/LongRunningBackups.json
- stable/2023-12-30/Configurations.json
- stable/2023-12-30/Databases.json
- stable/2023-12-30/FirewallRules.json
- stable/2023-12-30/LogFiles.json
- stable/2023-12-30/ServiceOperations.json
- stable/2023-12-30/Maintenances.json
- preview/2024-06-01-preview/FlexibleServers.json
- preview/2024-06-01-preview/AdvancedThreatProtectionSettings.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    from: LongRunningBackups.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutResponseCodes
    from: AdvancedThreatProtectionSettings.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
```

### Tag: package-flexibleserver-2024-10-01-preview

These settings apply only when `--tag=package-flexibleserver-2024-10-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2024-10-01-preview'
input-file:
- stable/2023-12-30/AzureADAdministrator.json
- stable/2023-12-30/Backups.json
- stable/2023-12-30/BackupAndExport.json
- stable/2023-12-30/LongRunningBackups.json
- stable/2023-12-30/Configurations.json
- stable/2023-12-30/Databases.json
- stable/2023-12-30/FirewallRules.json
- preview/2024-10-01-preview/FlexibleServers.json
- preview/2024-10-01-preview/AdvancedThreatProtectionSettings.json
- stable/2023-12-30/LogFiles.json
- preview/2024-10-01-preview/ServiceOperations.json
- stable/2023-12-30/Maintenances.json
suppressions:
  - code: PostOperationAsyncResponseValidation
    from: FlexibleServers.json
    reason: This check is optional.
  - code: PutResponseCodes
    from: LongRunningBackups.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutResponseCodes
    from: AdvancedThreatProtectionSettings.json
    reason: "202 is a pattern that is already used in our existing resources and being carried forward to new implementations to maintain consistency for our customers. This has already been approved by the API review board."
  - code: PutInOperationName
    from: AdvancedThreatProtectionSettings.json
    reason: "This API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario"
  - code: AllProxyResourcesShouldHaveDelete
    from: AdvancedThreatProtectionSettings.json
    reason: "PUT API is used to update thread detecion configuration, which is required by ARM policy, especially for `deployIfNotExist` scenario, we do not support DELETE operation"
```

### Tag: package-flexibleserver-2023-06-30-privatelink

These settings apply only when `--tag=package-flexibleserver-2023-06-30-privatelink` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2023-06-30-privatelink'
input-file:
- common-types/v1/common-types.json
- stable/2023-06-30/PrivateEndpointConnections.json
- stable/2023-06-30/PrivateLinkResources.json
suppressions:
  - code: PropertiesTypeObjectNoDefinition
    from: common-types.json
    reason: This will be fixed in new versions.
```

### Tag: package-flexibleserver-2022-01-01

These settings apply only when `--tag=package-flexibleserver-2022-01-01` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2022-01-01'
input-file:
- stable/2022-01-01/Backups.json
- stable/2022-01-01/Configurations.json
- stable/2022-01-01/Databases.json
- stable/2022-01-01/FirewallRules.json
- stable/2022-01-01/FlexibleServers.json
- stable/2022-01-01/LogFiles.json
- stable/2022-01-01/ServiceOperations.json
- stable/2022-01-01/AzureADAdministrator.json
```

### Tag: package-flexibleserver-2022-09-30-preview-privatelink

These settings apply only when `--tag=package-flexibleserver-2022-09-30-preview-privatelink` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2022-09-30-preview-privatelink'
input-file:
- preview/2021-12-01-preview/Backups.json
- preview/2021-12-01-preview/Configurations.json
- preview/2021-12-01-preview/Databases.json
- preview/2021-12-01-preview/FirewallRules.json
- preview/2021-12-01-preview/FlexibleServers.json
- preview/2021-12-01-preview/LogFiles.json
- preview/2021-12-01-preview/ServiceOperations.json
- preview/2021-12-01-preview/AzureADAdministrator.json
- preview/2022-09-30-preview/PrivateEndpointConnections.json
- preview/2022-09-30-preview/PrivateLinkResources.json
```

## Suppression

``` yaml
directive:
  - suppress: PathResourceProviderNamePascalCase
    reason: The name of the provider is Microsoft.DBforMySQL
  - suppress: OperationsApiResponseSchema
    from: mysql.json
    reason: Property isDataAction is not included in get operation reponse body
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-node
  - repo: azure-resource-manager-schemas
  - repo: azure-powershell
```

## Python

See configuration in [readme.python.md](./readme.python.md)

## Go

See configuration in [readme.go.md](./readme.go.md)

## Java

See configuration in [readme.java.md](./readme.java.md)
