---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ExportPersonalDataPostRequestBody(
	storage_location = "MyStorageAccount",
)

await graph_client.directory.inbound_shared_user_profiles.by_inbound_shared_user_profile_id('inboundSharedUserProfile-userId').export_personal_data.post(body = request_body)


```