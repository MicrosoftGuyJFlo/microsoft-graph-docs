---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Applications

$params = @{
	PrincipalId = "7679d9a4-2323-44cd-b5c2-673ec88d8b12"
	ResourceId = "076e8b57-bac8-49d7-9396-e3449b685055"
	AppRoleId = "00000000-0000-0000-0000-000000000000"
}

New-MgGroupAppRoleAssignment -GroupId $groupId -BodyParameter $params

```