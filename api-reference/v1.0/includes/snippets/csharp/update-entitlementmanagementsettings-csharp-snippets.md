---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var entitlementManagementSettings = new EntitlementManagementSettings
{
	ExternalUserLifecycleAction = AccessPackageExternalUserLifecycleAction.None
};

await graphClient.IdentityGovernance.EntitlementManagement.Settings
	.Request()
	.UpdateAsync(entitlementManagementSettings);

```