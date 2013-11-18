Get activities
==============

Get a list of a user's activities.


Parameters
----
`request` The request identifier. To perform this API request, set this to 'get_activities'.

`author` The user's username. 


Example POST
`
request = get_activities
author = rsmith
`

Returns a complete list of user's activities.
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<author>Rob</author>
	<activities>
		<activity1>
			<id>54</id>
			<title>Wednesday run</title>
			<date>1198053480</date>
		</activity1>
		<activity2>
			<id>500</id>
			<title>Bike ride home</title>
			<date>1223050320</date>
		</activity2>
		<activity3>
			<id>569</id>
			<title>Westgate to herne</title>
			<date>1223126383</date>
		</activity3>
	</activities>
</message>
```
