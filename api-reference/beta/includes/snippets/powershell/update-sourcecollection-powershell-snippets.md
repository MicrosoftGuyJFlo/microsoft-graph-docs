---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Compliance

$params = @{
	DisplayName = "Quarterly Financials search"
}

Update-MgComplianceEdiscoveryCaseSourceCollection -CaseId $caseId -SourceCollectionId $sourceCollectionId -BodyParameter $params

```