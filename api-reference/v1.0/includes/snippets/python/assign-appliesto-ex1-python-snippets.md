---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/v1.0/policies/appManagementPolicies/{id}",
)

await graph_client.applications.by_application_id('application-id').app_management_policies.ref.post(body = request_body)


```