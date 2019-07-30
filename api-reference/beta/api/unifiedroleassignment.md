---
title: "unifiedRoleAssignment resource type"
description: "PROVIDE DESCRIPTION HERE"
localization_priority: Normal
author: ""
ms.prod: ""
doc_type: "resourcePageType"
---

# unifiedRoleAssignment resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

PROVIDE DESCRIPTION HERE

## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get unifiedRoleAssignment](../api/unifiedroleassignment-get.md) | [unifiedRoleAssignment](unifiedroleassignment.md) | Read properties and relationships of unifiedRoleAssignment object. |
| [Create principal](../api/unifiedroleassignment-post-principal.md) | [directoryObject](directoryobject.md) | Create a new principal by posting to the principal collection. |
| [List principal](../api/unifiedroleassignment-list-principal.md) | [directoryObject](directoryobject.md) collection | Get a principal object collection. |
| [Create unifiedRoleDefinition](../api/unifiedroleassignment-post-roledefinition.md) | [unifiedRoleDefinition](unifiedroledefinition.md) | Create a new unifiedRoleDefinition by posting to the roleDefinition collection. |
| [List roleDefinition](../api/unifiedroleassignment-list-roledefinition.md) | [unifiedRoleDefinition](unifiedroledefinition.md) collection | Get a unifiedRoleDefinition object collection. |
| [Update](../api/unifiedroleassignment-update.md) | [unifiedRoleAssignment](unifiedroleassignment.md) | Update unifiedRoleAssignment object. |
| [Delete](../api/unifiedroleassignment-delete.md) | None | Delete unifiedRoleAssignment object. |

## Properties

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|id|String| Read-only.|
|principalId|String||
|resourceScope|String||
|roleDefinitionId|String||

## Relationships

| Relationship | Type        | Description |
|:-------------|:------------|:------------|
|principal|[directoryObject](directoryobject.md) collection| Read-only. Nullable.|
|roleDefinition|[unifiedRoleDefinition](unifiedroledefinition.md) collection| Read-only. Nullable.|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.unifiedRoleAssignment",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id": "String (identifier)",
  "principalId": "String",
  "resourceScope": "String",
  "roleDefinitionId": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "unifiedRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->