---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ActivityBasedTimeoutPolicy(
	definition = [
		"definition-value",
	]
	display_name = "displayName-value",
	is_organization_default = True,
)

result = await graph_client.policies.activity_based_timeout_policies.by_activity_based_timeout_policie_id('activityBasedTimeoutPolicy-id').patch(body = request_body)


```