Get activities
==============

Get a list of a user's latest activities.


Parameters
----
`request` The request identifier. To perform this API request, set this to 'get_activities'.

`author` The user's username. 

`offset` Offset the results by this amount. 


Example POST
----
`
request=get_activities&author=rsmith
`

Returns a list of user's latest activities.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
	<author>Rob</author>
	<activities>
		<activity1>
			<id>123</id>
			<title>
				<![CDATA[ Turbo session ]]>
			</title>
			<date>1485802037</date>
			<activity_type>Indoor cycling</activity_type>
			<distance>14.71356</distance>
			<moving_time>1938</moving_time>
			<elapsed_time>1938</elapsed_time>
			<speed_average>27.33169040247678</speed_average>
			<calories>400</calories>
			<effort>34</effort>
			<comment_count>3</comment_count>
			<like_count>2</like_count>
		</activity1>
		<activity2>
			<id>456</id>
			<title>
				<![CDATA[ Ride Home ]]>
			</title>
			<date>1445802021</date>
			<activity_type>Cycling</activity_type>
			<distance>9.52345</distance>
			<moving_time>912</moving_time>
			<elapsed_time>985</elapsed_time>
			<speed_average>21.63456323</speed_average>
			<calories>120</calories>
			<effort>14</effort>
			<comment_count>2</comment_count>
			<like_count>1</like_count>
		</activity2>
		<activity3>
			<id>789</id>
			<title>
				<![CDATA[ Westgate to herne ]]>
			</title>
			<date>1415402013</date>
			<activity_type>Cycling</activity_type>
			<distance>20.52345</distance>
			<moving_time>1895</moving_time>
			<elapsed_time>1953</elapsed_time>
			<speed_average>24.23452</speed_average>
			<calories>245</calories>
			<effort>19</effort>
			<comment_count />
			<like_count>5</like_count>
		</activity3>
	</activities>
</message>
```
