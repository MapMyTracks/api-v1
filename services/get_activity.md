Get activity
=====

Get a specific activity's location data.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'get_activity'.

`activity_id`
The id of an activity, as returned by the activities API service.

`from_time`
A UNIX timestamp from which location data will be returned.

Returns a list of positional data for the given activity, limited to 100 points, a note from the author and a flag identifiying whether the activity is live. Points are formatted in space delimeted blocks. Each block consists of the unixtime at which the location was recorded, followed by the location's latitude, longitude and altitude.

To get all location data within an activity with more than 100 points, call the API multiple times and modify the start_from parameter to suit.

Example POST
----
`request=get_activity&activity_id=54&from_time=0`

Returns the first 100 points for an activity.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>activity</type>
	<note>
		<![CDATA[ A bit cold this morning ]]>
	</note>
	<complete>Yes</complete>
	<points>
		1198052842,51.3704583333333,1.15737333333333,1.345 1198052846,51.370465,...
	</points>
</message>
```

In the event that the activity contains more than 100 points or the track is live, further requests are made to retrieve subsequent data in batches of 100 points.
