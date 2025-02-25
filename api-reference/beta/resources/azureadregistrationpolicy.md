---
title: "azureADRegistrationPolicy resource type"
description: "Represents the policy scope of a Microsoft Entra tenant that controls device registration using Microsoft Entra registered."
author: "myra-ramdenbourg"
ms.localizationpriority: medium
ms.prod: "directory-management"
doc_type: resourcePageType
---
# azureADRegistrationPolicy resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the policy scope of the Microsoft Entra tenant that controls the ability for users and groups to register device identities to your organization using **Microsoft Entra registered**. For more information, see [What is a device identity?](/azure/active-directory/devices/overview).

## Properties

|Property|Type|Description|
|:---|:---|:---|
|allowedGroups|String collection| The identifiers of the groups that are in the scope of the policy. Either this property or **allowedUsers** is required when the **appliesTo** property is set to `selected`. |
|allowedUsers|String collection| The identifiers of users that are in the scope of the policy. Either this property or **allowedGroups** is required when the **appliesTo** property is set to `selected`. |
|appliesTo|policyScope|Specifies whether to block or allow fine-grained control of the policy scope. The possible values are: `0` (meaning `none`), `1` (meaning `all`), `2` (meaning `selected`), `3` (meaning `unknownFutureValue`). <br/><br/>The default value is `1`. When set to `2`, at least one user or group identifier must be specified in either **allowedUsers** or **allowedGroups**.  Setting this property to `0` or `1` removes all identifiers in both **allowedUsers** and **allowedGroups**.|
|isAdminConfigurable|Boolean|Specifies whether this policy scope is configurable by the admin. The default value is `false`. When an admin has enabled Intune (MEM) to manage devices, this property is set to `false` and **appliesTo** defaults to `1` (meaning `all`). |

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.azureADRegistrationPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.azureADRegistrationPolicy",
  "appliesTo": "String",
  "isAdminConfigurable": "Boolean",
  "allowedUsers": [
    "String"
  ],
  "allowedGroups": [
    "String"
  ]
}
```
