---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Applications

$params = @{
	PrincipalId = "cde330e5-2150-4c11-9c5b-14bfdc948c79"
	ResourceId = "8e881353-1735-45af-af21-ee1344582a4d"
	AppRoleId = "00000000-0000-0000-0000-000000000000"
}

New-MgUserAppRoleAssignment -UserId $userId -BodyParameter $params

```