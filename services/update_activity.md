Update activity
====

Add new data to an activity.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'update_activity'.

`activity_id`
The unique id of the activity to which this update relates.

`points`
A list of points indicating new location(s) to append to this activity. The list of points should be space delimited in blocks containing latitude, longitude, altitude, and time data. These blocks are themselves space delimited.

Optional parameters
---
`hr`
Heart rate data (bpm) containing heartrate and time data delimited by a space

`cad`
Cadence data (rpm) containing heartrate and time data delimited by a space

`pwr`
Power data (watts) containing heartrate and time data delimited by a space

Returns - If the request was successful, the XML response will contain a message indicating that the activity has been updated. If the point data supplied was in an incorrect format, the XML response will indicate an error.

Example POST
---
```
request=update_activity&activity_id=9346&points=51.3704583333333%201.15737333333333%201.345%201198052842%2051.3704586%201.1573741%201.345%201198052844hr=80%201198052842%2090%201198052848&cad=33%201198052842%2044%201198052848&pwr=110%201198052842%20125%201198052848
```

Returns a message indicating that the activity has been updated.

**Reponse:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>activity_updated</type>
</message>
```
