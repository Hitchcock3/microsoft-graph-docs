---
title: "Get servicePrincipalRiskDetection"
description: "Read the properties and relationships of a servicePrincipalRiskDetection object."
author: "ebasseri"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Get servicePrincipalRiskDetection
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [servicePrincipalRiskDetection](../resources/serviceprincipalriskdetection.md) object.

>**Note:** You must have an Azure AD Premium P1 or P2 license to use the servicePrincipalRiskDetection API.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|IdentityRiskyServicePrincipal.Read.All, IdentityRiskyServicePrincipal.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|IdentityRiskyServicePrincipal.Read.All, IdentityRiskyServicePrincipal.ReadWrite.All|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /identityProtection/servicePrincipalRiskDetections/{servicePrincipalRiskDetectionId}
```
## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [servicePrincipalRiskDetection](../resources/serviceprincipalriskdetection.md) object in the response body.

## Examples

### Example 1: Get a specific risk detection object

#### Request
<!-- {
  "blockType": "request",
  "name": "get_serviceprincipalriskdetection"
}
-->
``` http
GET https://graph.microsoft.com/beta/identityProtection/servicePrincipalRiskDetections/{servicePrincipalRiskDetectionId}
```


#### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.servicePrincipalRiskDetection"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.servicePrincipalRiskDetection",
    "id": "2856d6e87c5c3a74021ff70291fa68107570c150d8dc145bdea5",
    "requestId": null,
    "correlationId": null,
    "riskEventType": "investigationsThreatIntelligence",
    "riskState": "atRisk",
    "riskLevel": "high",
    "riskDetail": "none",
    "source": "IdentityProtection",
    "detectionTimingType": "offline",
    "activity": "servicePrincipal",
    "tokenIssuerType": "AzureAD",
    "ipAddress": null,
    "location": null,
    "activityDateTime": "2021-10-26T00:00:00Z",
    "detectedDateTime": "2021-10-26T00:00:00Z",
    "lastUpdatedDateTime": "2021-10-26T16:28:17.8202975Z)",
    "servicePrincipalId": "99b8d28b-11ae-4e84-9bef-0e767e286grg",
    "servicePrincipalDisplayName": "Contoso App",
    "appId": "0grb38ac-a572-491d-a9db-b07197643457",
    "keyIds": [
      "9d9fea30-d8e3-481b-b57c-0ef569a989e5"
    ],
    "additionalInfo": "[{\"Key\":\"alertUrl\",\"Value\":null}]"
  }
}
```

