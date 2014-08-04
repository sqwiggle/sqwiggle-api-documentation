# User
A user object represents a single person on your organizations team.

## Attributes
<table>
    <tr>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <td>role</td>
        <td>enum</td>
        <td>user, owner, manager or banned</td>
    </tr>
    <tr>
        <td>media_device_id</td>
        <td>string</td>
        <td>A string representing current device that media is being received on</td>
    </tr>
    <tr>
        <td>status</td>
        <td>enum</td>
        <td>busy, available</td>
    </tr>
    <tr>
        <td>message</td>
        <td>string</td>
        <td>A status message that other users see, such as “out for lunch”</td>
    </tr>
    <tr>
        <td>name</td>
        <td>string</td>
        <td>The users full name</td>
    </tr>
    <tr>
        <td>email</td>
        <td>string</td>
        <td>The users email address</td>
    </tr>
    <tr>
        <td>avatar</td>
        <td>string</td>
        <td>URL to a static avatar for the user</td>
    </tr>
    <tr>
        <td>snapshot</td>
        <td>string</td>
        <td>URL to the last snapshot for this user (auto or manual)</td>
    </tr>
    <tr>
        <td>snapshot_interval</td>
        <td>integer</td>
        <td>Frequency at which automatic snapshots are taken when the app is open</td>
    </tr>
    <tr>
        <td>confirmed</td>
        <td>boolean</td>
        <td>The users email confirmation status</td>
    </tr>
    <tr>
        <td>time_zone</td>
        <td>string</td>
        <td>Timezone (rails format)</td>
    </tr>
    <tr>
        <td>time_zone_offset</td>
        <td>float</td>
        <td>Hours offset from UTC, note that this may be a non-integer like 5.5</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time this user was created</td>
    </tr>
    <tr>
        <td>last_active_at</td>
        <td>datetime</td>
        <td>The last time we recorded activity for a user</td>
    </tr>
    <tr>
        <td>last_connected_at</td>
        <td>datetime</td>
        <td>The time this users current online session started</td>
    </tr>
</table>

## Example

    {   
        "id": 1234,
        "role": "user",
        "name": "John Doe",
        "media_device_id": "53d4bb00-f25f-6322-4176-a35aed5a12a5",
        "status": "busy",
        "message": "In a meeting",
        "email": "john.doe@gmail.com",,
        "avatar": "http://sqwiggle-photos.amazonaws.com/images/avatar.jpg",
        "snapshot": "http://sqwiggle-photos.amazonaws.com/images/snapshot.jpg",
        "snapshot_interval": 60,
        "confirmed": true,
        "time_zone": "America/New_York",
        "time_zone_offset": 5.0,
        "created_at": "2013-01-01T03:18:33Z",
        "last_connected_at": "2013-07-20T20:10:33Z",
        "last_active_at": "2013-07-20T20:18:33Z"
    }
