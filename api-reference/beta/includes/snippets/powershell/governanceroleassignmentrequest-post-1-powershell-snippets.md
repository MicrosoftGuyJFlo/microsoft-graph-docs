---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Identity.Governance

$params = @{
	RoleDefinitionId = "ea48ad5e-e3b0-4d10-af54-39a45bbfe68d"
	ResourceId = "e5e7d29d-5465-45ac-885f-4716a5ee74b5"
	SubjectId = "918e54be-12c4-4f4c-a6d3-2ee0e3661c51"
	AssignmentState = "Eligible"
	Type = "AdminAdd"
	Reason = "Assign an eligible role"
	Schedule = @{
		StartDateTime = [System.DateTime]::Parse("2018-05-12T23:37:43.356Z")
		EndDateTime = [System.DateTime]::Parse("2018-11-08T23:37:43.356Z")
		Type = "Once"
	}
}

New-MgPrivilegedAccessRoleAssignmentRequest -PrivilegedAccessId $privilegedAccessId -BodyParameter $params

```