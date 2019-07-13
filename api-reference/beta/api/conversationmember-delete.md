---
title: "Delete conversationMember"
description: "Delete a conversationMember from a channel."
author: "clearab"
doc_type: "apiPageType"
localization_priority: Normal
ms.prod: "microsoft-teams"
---

# Delete conversationMember

[!INCLUDE [private-preview-disclaimer](../../includes/private-preview-disclaimer.md)]

Delete a [conversationMember](../resources/conversationmember.md) from a [channel](../resources/channel.md).

> [!NOTE]
>This operation is only supported on channels with a [channelMembershipType](../resources/enums.md#channelMembershipType-values) of `private`. Calls with any other [channelMembershipType](../resources/enums.md#channelMembershipType-values) will return a 400 Bad Request response.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission Type|Permissions (from least to most privileged)|
|---------|-------------|
|Delegated (work or school account)|Group.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|Group.ReadWrite.All|

## HTTP request
<!-- { "blockType": "ignored"} -->
```http
DELETE /teams/{id}/channels/{id}/members/{id}
```

## Request headers

| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Example

### Request

Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "delete_conversation_member"
} -->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}/members/{id}
```

### Response

Here is an example of the response.

<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
```