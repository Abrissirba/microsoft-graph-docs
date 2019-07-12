---
title: "Install app for user"
description: "Installs an app in the personal scope of the specified user."
author: "anandjo"
localization_priority: Normal
ms.prod: "microsoft-teams"
---

# Install app for user

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Installs an [app](../resources/teamsapp.md) in the personal scope of the specified [user](../resources/user.md).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  User.ReadWrite.All, Directory.ReadWrite.All     |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | User.ReadWrite.All, Directory.ReadWrite.All |

## HTTP request

```http
POST /users/{id}/teamwork/installedApps
```

## Request headers

| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body

| Property   | Type |Description|
|:---------------|:--------|:----------|
|teamsApp|String|The id of the app to add.|

## Response

If successful, this method returns a `201 OK` response code.

## Example

#### Request

The following is an example of the request.

```http
POST https://graph.microsoft.com/beta/users/{id}/teamwork/installedApps
{
   "teamsApp@odata.bind":"https://graph.microsoft.com/beta/appCatalogs/teamsApps/12345678-9abc-def0-123456789a"
}
```

#### Response

The following is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsAppInstallation",
  "isCollection": true
} -->

```http
HTTP/1.1 201 OK
Content-type: application/json
Content-length: 0
```

## See also

- [List apps installed for a user](../api/teamsappinstallation-user-list.md)
- [Uninstall app for a user](../api/teamsappinstallation-user-delete.md)
- [Upgrade installed app for a user](../api/teamsappinstallation-user-upgrade.md)
