Delete activity
=====

Deletes an activity and all its associated data.

Parameters
---

`request`
The request identifier. To perform this API request, set this to 'delete_activity'.

`activity_id`
The id of an activity, as returned by the activities API service.

Example POST
----
`request=delete_activity&activity_id=54`

Deletes an activity and all its associated data.
The username and password provided must match the respective activity's author in order to be authorised.

**Response:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
  <type>activity_deleted</type>
</message>
```

**Error:**
```
<?xml version="1.0" encoding="UTF-8"?>
<message>
  <type>invalid_activity_id</type>
</message>
```

```
<?xml version="1.0" encoding="UTF-8"?>
<message>
  <type>unauthorized</type>
</message>
```
