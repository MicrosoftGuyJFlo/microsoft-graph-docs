---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Identity.SignIns

$params = @{
	Key = "key-value"
}

Invoke-MgUploadTrustFrameworkKeySetCertificate -TrustFrameworkKeySetId $trustFrameworkKeySetId -BodyParameter $params

```