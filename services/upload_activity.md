Upload activity
====
Upload an activity in it's entirety, in GPX format

Parameters
---
`request`
The request identifier. To perform this API request, set this to 'upload_activity'.

`gpx_file`
A GPX file formatted representation of the activity

`status`
Indicates if this activity is to be public or privately visible. Possible values are "public" and "private".

`description`
The request identifier. To perform this API request, set this to 'get_time'.

`activity`
The activity type. Possible values are "running", "cycling", "mountain biking", "indoor cycling", "sailing", "walking", "hiking", "driving", "motor racing", "off road driving", "motorcycling", "enduro", "skiing", "cross country skiing", "canoeing", "kayaking", "sea kayaking", "stand up paddle boarding", "rowing", "windsurfing", "kiteboarding", "orienteering", "mountaineering", "skating", "skateboarding", "longboarding", "horse riding", "hang gliding", "gliding", "flying", "snowboarding", "paragliding", "hiking", "hot air ballooning", "stand up paddle boarding" and "nordic walking".

Returns an XML formatted replay indicating success or failure.
If success, returns the entry_id for the new activity.

Example POST
---
(gpx_file has been truncated for clarity)

```
request=upload_activity&gpx_file=<?xml...&status=public&description=My%20weekend%20run&activity=running
```

**Success:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>success</type>
	<id>12345678</id>
</message>
```

**Error:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<type>error</type>
</message>
```
