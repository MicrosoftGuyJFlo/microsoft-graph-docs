---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.IdentityGovernance.EntitlementManagement.AccessPackageAssignmentRequests["{accessPackageAssignmentRequest-id}"]
	.Request()
	.DeleteAsync();

```