---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = EdiscoveryReviewTag(
	display_name = "My tag API",
	description = "Use Graph API to create tags",
	child_selectability = ChildSelectability.Many,
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').tags.post(body = request_body)


```