Get activity tags
=====

Get tags for an activity.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'get_activity_tags'.

`activity_id`
The id of an activity, as returned by the activities API service.

Returns a list of tags for an activity.

Example POST
----
`request=get_activity_tags&activity_id=54`

Returns activity tags.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
  <tags>
    <tag1>
      <name>
        <![CDATA[ RideToLondon ]]>
      </name>
      <date>1484074832</date>
    </tag1>
    <tag2>
      <name>
        <![CDATA[ CharityCycle ]]>
      </name>
      <date>1384074832</date>
    </tag2>
  </tags>
</message>
```
