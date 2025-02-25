---
title: "privilegedAccessGroupEligibilityScheduleInstance: filterByCurrentUser"
description: "Return instances of membership and ownership eligibility schedules for the calling principal."
author: "ilyalushnikov"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: apiPageType
---

# privilegedAccessGroupEligibilityScheduleInstance: filterByCurrentUser
Namespace: microsoft.graph

Return instances of membership and ownership eligibility schedules for the calling principal.

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|PrivilegedEligibilitySchedule.Read.AzureADGroup, PrivilegedEligibilitySchedule.ReadWrite.AzureADGroup|
|Delegated (personal Microsoft account)|Not supported.|
|Application|PrivilegedEligibilitySchedule.Read.AzureADGroup, PrivilegedEligibilitySchedule.ReadWrite.AzureADGroup|

[!INCLUDE [rbac-pim-groups-apis-read-eligibilityschedules](../includes/rbac-for-apis/rbac-pim-groups-apis-read-eligibilityschedules.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /identityGovernance/privilegedAccess/group/eligibilityScheduleInstances/filterByCurrentUser(on='parameterValue')
```

## Function parameters
In the request URL, provide the following query parameters with values.
The following table shows the parameters that must be used with this function.

|Parameter|Type|Description|
|:---|:---|:---|
|on|eligibilityScheduleInstanceFilterByCurrentUserOptions|Filter used to query eligibilityScheduleInstances. The possible values are `principal`, `unknownFutureValue`. Required.|


## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [privilegedAccessGroupEligibilityScheduleInstance](../resources/privilegedaccessgroupeligibilityscheduleinstance.md) collection in the response body.

## Examples

### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "privilegedaccessgroupeligibilityscheduleinstancethis.filterbycurrentuser"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/identityGovernance/privilegedAccess/group/eligibilityScheduleInstances/filterByCurrentUser(on='principal')
```


### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.privilegedAccessGroupEligibilityScheduleInstance)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.privilegedAccessGroupEligibilityScheduleInstance",
      "id": "8MYkhImhnkm70CbBdTyW1BbHHAdHgZdDpbqyEFlRzAs-1-e",
      "startDateTime": "2022-04-12T14:44:50.287Z",
      "endDateTime": "2024-04-10T00:00:00Z",
      "memberType": "Direct",
      "principalId": "3cce9d87-3986-4f19-8335-7ed075408ca2",
      "accessId": "member",
      "groupId": "2b5ed229-4072-478d-9504-a047ebd4b07d",
      "eligibilityScheduleId": "77f71919-62f3-4d0c-9f88-0a0391b665cd"
    }
  ]
}
```
