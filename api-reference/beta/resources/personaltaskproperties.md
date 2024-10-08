---
title: "personalTaskProperties resource type"
description: Contains personal properties of a task"
author: "avijityadav"
ms.localizationpriority: medium
ms.prod: "outlook"
doc_type: resourcePageType
---

# personalTaskProperties resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Contains personal properties of a [task](task.md). When sharing or assigning a **task**, these properties will not be seen by other users.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|reminderDatetime|[dateTimeTimeZone](../resources/datetimetimezone.md)|The date and time for a reminder alert of the **task** to occur.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.personalTaskProperties"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.personalTaskProperties",
  "reminderDatetime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  }
}
```

