---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = IdentityUserFlowAttributeAssignment(
	is_optional = False,
	requires_verification = False,
	user_input_type = IdentityUserFlowAttributeInputType.TextBox,
	display_name = "Shoe size",
	user_attribute_values = [
	]
	user_attribute = IdentityUserFlowAttribute(
		id = "extension_guid_shoeSize",
	),
)

result = await graph_client.identity.b2c_user_flows.by_b2c_user_flow_id('b2cIdentityUserFlow-id').user_attribute_assignments.post(body = request_body)


```