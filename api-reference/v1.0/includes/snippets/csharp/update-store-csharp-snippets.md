---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var store = new Microsoft.Graph.TermStore.Store
{
	DefaultLanguageTag = "en-US"
};

await graphClient.Sites["{site-id}"].TermStore
	.Request()
	.UpdateAsync(store);

```