Get user
==============

Get information about a user.


Parameters
----
`request` The request identifier. To perform this API request, set this to 'get_user'.


Example POST
----
`
request=get_user
`

Returns information about a user.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
  <type>user</type>
  <plus>true</plus>
  <screen_name><![CDATA[ John Smith ]]></screen_name>
</message>
```
