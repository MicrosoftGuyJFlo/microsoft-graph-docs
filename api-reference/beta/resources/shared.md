---
author: JeremyKelley
description: "The Shared resource indicates a DriveItem has been shared with others."
ms.date: 09/10/2017
title: Shared
ms.localizationpriority: medium
doc_type: resourcePageType
ms.prod: ""
---
# Shared resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **Shared** resource indicates a DriveItem has been shared with others.
The resource includes information about how the item is shared.

If a [**Driveitem**](driveitem.md) has a non-null **shared** facet, the item has been shared.

## JSON representation

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.shared",
  "optionalProperties": [ "sharedBy", "sharedDateTime" ]
}-->

```json
{
  "owner": { "@odata.type": "microsoft.graph.identitySet" },
  "scope": "anonymous | organization | users",
  "sharedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "sharedDateTime": "datetime"
}
```

## Properties

| Property       | Type                          | Description
| :------------- |:------------------------------|:----------------------------
| owner          | [IdentitySet](identityset.md) | The identity of the owner of the shared item. Read-only.
| scope          | String                        | Indicates the scope of how the item is shared: `anonymous`, `organization`, or `users`. Read-only.
| sharedBy       | [identitySet](identityset.md) | The identity of the user who shared the item. Read-only.
| sharedDateTime | DateTimeOffset                | The UTC date and time when the item was shared. Read-only.

## Scope values

| Value          | Description                                                                           |
|:---------------|:--------------------------------------------------------------------------------------|
| `anonymous`    | The item is shared by using a link that works for anyone with the link.               |
| `organization` | The item is shared by using a link that works for anyone in the owner's organization. |
| `users`        | The item is shared with specific users only.                                          |

## Remarks

For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).

<!--
{
  "type": "#page.annotation",
  "description": "The shared facet provides info about shared items.",
  "keywords": "shared,share,item,facet,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Shared",
  "suppressions": []
}
-->


