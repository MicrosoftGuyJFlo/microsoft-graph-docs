---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messages = await graphClient.Chats["{chat-id}"].Messages
	.Request()
	.OrderBy("createdDateTime")
	.Top(2)
	.GetAsync();

```