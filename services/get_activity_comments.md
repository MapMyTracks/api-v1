Get activity comments
=====

Get comments for an activity.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'get_activity_comments'.

`activity_id`
The id of an activity, as returned by the activities API service.

Returns a list of comments, with their respective authors, for an activity.

Example POST
----
`request=get_activity_comments&activity_id=54`

Returns activity comments.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
  <comments>
    <comment1>
      <id>123</id>
      <comment>
        <![CDATA[ Good job ]]>
      </comment>
      <author>
        <![CDATA[ Bret ]]>
      </author>
      <author_id>52345</author_id>
      <date>1306428893</date>
    </comment1>
    <comment2>
      <id>456</id>
      <comment>
        <![CDATA[ Nice ride! ]]>
      </comment>
      <author>
        <![CDATA[ Bob123 ]]>
      </author>
      <author_id>12436</author_id>
      <date>1309328149</date>
    </comment2>
  </comments>
</message>
```
