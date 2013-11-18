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
request = update_activity
activity_id = 9346
points = 51.3704583333333 1.15737333333333 1.345 1198052842 51.3704586 
1.1573741 1.345 1198052844
hr = 80 1198052842 90 1198052848
cad = 33 1198052842 44 1198052848
pwr = 110 1198052842 125 1198052848
```

Returns a message indicating that the activity has been updated.

*Reponse:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>activity_updated</type>
</message>
```
