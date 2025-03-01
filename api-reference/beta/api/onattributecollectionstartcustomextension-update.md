---
title: "Update onAttributeCollectionStartCustomExtension"
description: "Associate a custom extension with an onAttributeCollectionStartCustomExtension object that's linked to an onAttributeCollectionStartListener object."
author: "nanguil"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Update onAttributeCollectionStartCustomExtension

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Associate a custom extension with an [onAttributeCollectionStartCustomExtension](../resources/onattributecollectionstartcustomextension.md) object that's linked to an [onAttributeCollectionStartListener](../resources/onattributecollectionstartlistener.md).

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "onattributecollectionstartcustomextension-update-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/onattributecollectionstartcustomextension-update-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PUT /identity/authenticationEventListeners/{listenerId}/microsoft.graph.onAttributeCollectionStartListener/handler/microsoft.graph.onAttributeCollectionStartCustomExtensionHandler/customExtension/$ref
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body

In the request body, supply the **@odata.id** property with the absolute URL of the [customAuthenticationExtension](../resources/customauthenticationextension.md) object that you want to associate with the [onAttributeCollectionStartCustomExtension](../resources/onattributecollectionstartcustomextension.md) object that's linked to the [onAttributeCollectionStartListener](../resources/onattributecollectionstartlistener.md).

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following example shows a request.
# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_onattributecollectionstartcustomextension"
}
-->
``` http
PUT https://microsoft.graph.microsoft.com/beta/identity/authenticationEventListeners/{listenerId}/microsoft.graph.onAttributeCollectionStartListener/handler/microsoft.graph.onAttributeCollectionStartCustomExtensionHandler/customExtension/$ref
Content-Type: application/json

{
  "@odata.id": "https://graph.microsoft.com/beta/identity/customAuthenticationExtensions/{customExtensionId}"
}
```

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-onattributecollectionstartcustomextension-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-onattributecollectionstartcustomextension-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### Response

The following example shows the response.
<!-- {
  "blockType": "response"
}
-->
``` http
HTTP/1.1 204 No Content
```

