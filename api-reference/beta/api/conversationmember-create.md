---
title: "Add conversationMember"
description: "Add a member to a channel."
author: "dafranc"
localization_priority: Normal
ms.prod "microsoft-teams"
---

# Update conversationMember

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Add a [conversationMember](../resources/conversationmember.md) to a [channel](../resources/channel.md).

>**Note:** This operation is only supported on channels with a `channelType` of `private`

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
POST /teams/{id}/channels/{id}/members/{id}
```

## Optional query parameters

This operation does not support the [OData query parameters](/graph/query-parameters) to customize the response.

## Request headers

| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|roles|string collection|The roles for that user.|
|user|`user`|The user to add to the channel.|

## Response

If successful, this method returns a `201 Created` response code and a [conversationMember](../resources/conversationmember.md) object in the response body.

## Example

#### Request

Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_conversation_member"
} -->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels/{id}/members/
content-type: application/json
content-length: 26

{
  "@odata.type": "#microsoft.graph.aadConversationMember"
  "roles": [],
  "user@odata.bind": "https://graph.microsoft.com/beta/users('8b081ef6-4792-4def-b2c9-c363a1bf41d5')"
}
```

#### Response

Here is an example of the response.

>**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationMember"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length:

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#teams('ece6f0a1-7ca4-498b-be79-edf6c8fc4d82')/channels('19%3A56eb04e133944cf69e603c5dac2d292e%40thread.skype')/members/microsoft.graph.aadUserConversationMember/$entity"
  "@odata.type": "#microsoft.graph.aadUserConversationMember",
  "id": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
  "roles": [],
  "displayName": "John Doe",
  "userId": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
  "email": null
}
```