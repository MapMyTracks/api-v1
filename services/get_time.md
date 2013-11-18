Get time
====
Get the Map My Tracks server's current system time.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'get_time'.

`Returns`
The XML response contains the current system time.

Example POST
---

`request=get_time`

Returns the current system time.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>time</type>
	<server_time>1242988693</server_time>
</message>
```
