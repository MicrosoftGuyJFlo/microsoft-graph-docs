---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Users

$params = @{
	DisplayName = "Travel items"
}

# A UPN can also be used as -UserId.
New-MgUserTodoList -UserId $userId -BodyParameter $params

```