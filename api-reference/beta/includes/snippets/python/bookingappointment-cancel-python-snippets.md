---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = CancelPostRequestBody(
	cancellation_message = "Your appointment has been successfully cancelled. Please call us again.",
)

await graph_client.booking_businesses.by_booking_businesse_id('bookingBusiness-id').appointments.by_appointment_id('bookingAppointment-id').cancel.post(body = request_body)


```