Stop activity
====

Stop the tracking of an activity.

Parameters
---
`request`
The request identifier. To perform this API request, set this to 'stop_activity'.

Returns the XML reponse will contain a message indicating that the activity has been stopped.

Example POST
---
`request=stop_activity`

Returns a message indicating that the activity has been stopped.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>activity_stopped</type>
</message>
```
