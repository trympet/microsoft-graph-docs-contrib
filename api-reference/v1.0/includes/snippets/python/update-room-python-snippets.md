---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = Room(
	odata_type = "microsoft.graph.room",
	nickname = "Conf Room",
	building = "1",
	label = "100",
	capacity = 50,
	is_wheel_chair_accessible = False,
)

result = await graph_client.places.by_place_id('place-id').patch(body = request_body)


```