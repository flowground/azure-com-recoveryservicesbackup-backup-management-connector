# ![LOGO](logo.png) RecoveryServicesBackupClient **flow**ground Connector

## Description

A generated **flow**ground connector for the RecoveryServicesBackupClient API (version 2016-12-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/recoveryservicesbackup-backupManagement/2016-12-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:39+03:00

## API Description



## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Backup management servers registered to Recovery Services Vault. Returns a pageable list of servers.

*Tags:* `BackupEngines`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Returns backup management server registered to Recovery Services Vault.

*Tags:* `BackupEngines`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `backupEngineName` - _required_ - Name of the backup management server.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Provides the result of the refresh operation triggered by the BeginRefresh operation.

*Tags:* `ProtectionContainerRefreshOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the container.
* `operationId` - _required_ - Operation ID associated with the operation whose result needs to be fetched.

### Gets details of the specific container registered to your Recovery Services Vault.

*Tags:* `ProtectionContainers`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Name of the fabric where the container belongs.
* `containerName` - _required_ - Name of the container whose details need to be fetched.

### Fetches the result of any operation on the container.

*Tags:* `ProtectionContainerOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the container.
* `containerName` - _required_ - Container name whose information should be fetched.
* `operationId` - _required_ - Operation ID which represents the operation whose result needs to be fetched.

### Used to disable backup of an item within a container. This is an asynchronous operation. To know the status of the request, call the GetItemOperationResult API.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up item.
* `containerName` - _required_ - Container name associated with the backed up item.
* `protectedItemName` - _required_ - Backed up item to be deleted.

### Provides the details of the backed up item. This is an asynchronous operation. To know the status of the operation, call the GetItemOperationResult API.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up item.
* `containerName` - _required_ - Container name associated with the backed up item.
* `protectedItemName` - _required_ - Backed up item name whose details are to be fetched.
* `$filter` - _optional_ - OData filter options.

### Enables backup of an item or to modifies the backup policy information of an already backed up item. This is an asynchronous operation. To know the status of the operation, call the GetItemOperationResult API.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backup item.
* `containerName` - _required_ - Container name associated with the backup item.
* `protectedItemName` - _required_ - Item name to be backed up.

### Triggers backup for specified backed up item. This is an asynchronous operation. To know the status of the operation, call GetProtectedItemOperationResult API.

*Tags:* `Backups`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backup item.
* `containerName` - _required_ - Container name associated with the backup item.
* `protectedItemName` - _required_ - Backup item for which backup needs to be triggered.

### Fetches the result of any operation on the backup item.

*Tags:* `ProtectedItemOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backup item.
* `containerName` - _required_ - Container name associated with the backup item.
* `protectedItemName` - _required_ - Backup item name whose details are to be fetched.
* `operationId` - _required_ - OperationID which represents the operation whose result needs to be fetched.

### Fetches the status of an operation such as triggering a backup, restore. The status can be in progress, completed or failed. You can refer to the OperationStatus enum for all the possible states of the operation. Some operations create jobs. This method returns the list of jobs associated with the operation.

*Tags:* `ProtectedItemOperationStatuses`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backup item.
* `containerName` - _required_ - Container name associated with the backup item.
* `protectedItemName` - _required_ - Backup item name whose details are to be fetched.
* `operationId` - _required_ - OperationID represents the operation whose status needs to be fetched.

### Lists the backup copies for the backed up item.

*Tags:* `RecoveryPoints`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up item.
* `containerName` - _required_ - Container name associated with the backed up item.
* `protectedItemName` - _required_ - Backed up item whose backup copies are to be fetched.
* `$filter` - _optional_ - OData filter options.

### Provides the information of the backed up data identified using RecoveryPointID. This is an asynchronous operation. To know the status of the operation, call the GetProtectedItemOperationResult API.

*Tags:* `RecoveryPoints`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with backed up item.
* `containerName` - _required_ - Container name associated with backed up item.
* `protectedItemName` - _required_ - Backed up item name whose backup data needs to be fetched.
* `recoveryPointId` - _required_ - RecoveryPointID represents the backed up data to be fetched.

### Provisions a script which invokes an iSCSI connection to the backup data. Executing this script opens a file explorer displaying all the recoverable files and folders. This is an asynchronous operation. To know the status of provisioning, call GetProtectedItemOperationResult API.

*Tags:* `ItemLevelRecoveryConnections`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up items.
* `containerName` - _required_ - Container name associated with the backed up items.
* `protectedItemName` - _required_ - Backed up item name whose files/folders are to be restored.
* `recoveryPointId` - _required_ - Recovery point ID which represents backed up data. iSCSI connection will be provisioned for this backed up data.

### Restores the specified backed up data. This is an asynchronous operation. To know the status of this API call, use GetProtectedItemOperationResult API.

*Tags:* `Restores`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up items.
* `containerName` - _required_ - Container name associated with the backed up items.
* `protectedItemName` - _required_ - Backed up item to be restored.
* `recoveryPointId` - _required_ - Recovery point ID which represents the backed up data to be restored.

### Revokes an iSCSI connection which can be used to download a script. Executing this script opens a file explorer displaying all recoverable files and folders. This is an asynchronous operation.

*Tags:* `ItemLevelRecoveryConnections`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up items.
* `containerName` - _required_ - Container name associated with the backed up items.
* `protectedItemName` - _required_ - Backed up item name whose files/folders are to be restored.
* `recoveryPointId` - _required_ - Recovery point ID which represents backed up data. iSCSI connection will be revoked for this backed up data.

### Discovers all the containers in the subscription that can be backed up to Recovery Services Vault. This is an asynchronous operation. To know the status of the operation, call GetRefreshOperationResult API.

*Tags:* `ProtectionContainers`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated the container.

### Gets the operation result of operation triggered by Export Jobs API. If the operation is successful, then it also contains URL of a Blob and a SAS key to access the same. The blob contains exported jobs in JSON serialized format.

*Tags:* `ExportJobsOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `operationId` - _required_ - OperationID which represents the export job.

### Cancels a job. This is an asynchronous operation. To know the status of the cancellation, call GetCancelOperationResult API.

*Tags:* `JobCancellations`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `jobName` - _required_ - Name of the job to cancel.

### Fetches the result of any operation.<br/>
>             the operation.

*Tags:* `JobOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `jobName` - _required_ - Job name whose operation result has to be fetched.
* `operationId` - _required_ - OperationID which represents the operation whose result has to be fetched.

### Triggers export of jobs specified by filters and returns an OperationID to track.

*Tags:* `Jobs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.

### Provides the status of the delete operations such as deleting backed up item. Once the operation has started, the status code in the response would be Accepted. It will continue to be in this state till it reaches completion. On successful completion, the status code will be OK. This method expects OperationID as an argument. OperationID is part of the Location header of the operation response.

*Tags:* `BackupOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `operationId` - _required_ - OperationID which represents the operation.

### Fetches the status of an operation such as triggering a backup, restore. The status can be in progress, completed or failed. You can refer to the OperationStatus enum for all the possible states of an operation. Some operations create jobs. This method returns the list of jobs when the operation is complete.

*Tags:* `BackupOperationStatuses`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `operationId` - _required_ - OperationID which represents the operation.

### Lists of backup policies associated with Recovery Services Vault. API provides pagination parameters to fetch scoped results.

*Tags:* `BackupPolicies`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.

### Deletes specified backup policy from your Recovery Services Vault. This is an asynchronous operation. Status of the operation can be fetched using GetPolicyOperationResult API.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `policyName` - _required_ - Backup policy to be deleted.

### Provides the details of the backup policies associated to Recovery Services Vault. This is an asynchronous operation. Status of the operation can be fetched using GetPolicyOperationResult API.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `policyName` - _required_ - Backup policy information to be fetched.

### Creates or modifies a backup policy. This is an asynchronous operation. Status of the operation can be fetched using GetPolicyOperationResult API.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `policyName` - _required_ - Backup policy to be created.

### Provides the result of an operation.

*Tags:* `ProtectionPolicyOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `policyName` - _required_ - Backup policy name whose operation's result needs to be fetched.
* `operationId` - _required_ - Operation ID which represents the operation whose result needs to be fetched.

### Provides the status of the asynchronous operations like backup, restore. The status can be in progress, completed or failed. You can refer to the Operation Status enum for all the possible states of an operation. Some operations create jobs. This method returns the list of jobs associated with operation.

*Tags:* `ProtectionPolicyOperationStatuses`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `policyName` - _required_ - Backup policy name whose operation's status needs to be fetched.
* `operationId` - _required_ - Operation ID which represents an operation whose status needs to be fetched.

### Provides a pageable list of protectable objects within your subscription according to the query filter and the pagination parameters.

*Tags:* `BackupProtectableItems`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Provides a pageable list of all items that are backed up within a vault.

*Tags:* `BackupProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Lists the containers registered to Recovery Services Vault.

*Tags:* `BackupProtectionContainers`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.

### Get the security PIN.

*Tags:* `SecurityPINs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.

### Fetches the backup management usage summaries of the vault.

*Tags:* `BackupUsageSummaries`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Fetches resource vault config.

*Tags:* `BackupResourceVaultConfigs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.

### Updates vault security config.

*Tags:* `BackupResourceVaultConfigs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.

### Fetches resource storage config.

*Tags:* `BackupResourceStorageConfigs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.

### Updates vault storage model type.

*Tags:* `BackupResourceStorageConfigs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.

## License

**flow**ground :- Telekom iPaaS / azure-com-recoveryservicesbackup-backup-management-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
