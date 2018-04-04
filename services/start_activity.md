Start activity
====

Initiate the tracking of an activity.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'start_activity'.

`title`
The title of the new activity. The title must be no longer that 100 characters.

`privacy`
Indicates if this activity is to be public or privately visible. Possible values are "public" and "private".

`activity`
The activity type. Possible values are "running", "cycling", "mountain biking", "indoor cycling", "hand cycling", "sailing", "walking", "hiking", "driving", "motor racing", "off road driving", "motorcycling", "enduro", "skiing", "cross country skiing", "swimming", "canoeing", "kayaking", "sea kayaking", "stand up paddle boarding", "rowing", "windsurfing", "kiteboarding", "orienteering", "mountaineering", "skating", "skateboarding", "longboarding", "horse riding", "hang gliding", "gliding", "flying", "snowboarding", "paragliding", "hiking", "hot air ballooning", "snowshoeing", "nordic walking", "jet skiing", "powerboating" and "wheelchair".

`points`
A list of points indicating the location(s) that this track is to be initiated with. The list of points should be space delimited in blocks containing latitude, longitude, altitude, and time data. These blocks are themselves space delimited.

`source`
An identifier representing the source application from which this API call is being made.

`version`
The version of the source application.

Optional parameters
---

`tags`
A comma separated list of tags. Each tag must be no longer that 50 characters.

`hr`
Heart rate data (bpm) containing heartrate and time data delimited by a space

`cad`
Cadence data (rpm) containing heartrate and time data delimited by a space

`pwr`
Power data (watts) containing heartrate and time data delimited by a space

`unique_token`
A unique string (containing a concatenated representation of the calling device's serial number and current time, for example) that can be used to identify calls to start_activity in poor network areas where no reply (and therefore no activity_id) is received. This can be used to aviod the creation of multiple activities.

`version`
An identifier representing the version of the source application from which this API call is being made.

`Returns`
If the request was successful, the XML response will contain a unique activity id relating to the newly created activity. If the point data supplied was in an incorrect format, the XML response will indicate an error.

Example POST
----
```
request=start_activity&title=My%20activity&tags=training,whitstable&privacy=public&activity=running&source=My%20app&points=51.3704583333333%201.15737333333333%201.345%201198052842%2051.3704586%201.1573741%201.345%201198052844
```

Returns a message containing the newly created activity id.

**Reponse:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>activity_started</type>
	<activity_id>9346</activity_id>
</message>
```
