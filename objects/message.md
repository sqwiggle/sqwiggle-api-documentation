# Message
A message object represents an item in any chat stream, they may be created by humans, bots or the Sqwiggle servers.

## Attributes
<table>
    <tr>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <td>room_id</td>
        <td>integer</td>
        <td>Id of the room that this message belongs to</td>
    </tr>
    <tr>
        <td>message</td>
        <td>string</td>
        <td>The plain text content of the message, HTML will be escaped</td>
    </tr>
    <tr>
        <td>user</td>
        <td>User</td>
        <td>A partial user object representing the user that created the message</td>
    </tr>
    <tr>
        <td>attachments</td>
        <td>list</td>
        <td>A list of Attachment objects to be displayed with this message</td>
    </tr>
    <tr>
        <td>mentions</td>
        <td>list</td>
        <td>A list of users tagged / mentioned in this message</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time that this message was created</td>
    </tr>
    <tr>
        <td>updated_at</td>
        <td>datetime</td>
        <td>The time that this message was last updated or edited</td>
    </tr>
</table>


## Example

```
{
    "id": 1234,
    "room_id": 5678,
    "message": "Jack Dorsey, just setting up my sqwggl",
    "user": {
        "id": 9374,
        "name": "Ev",
        ...
    },
    "attachments": [],
    "mentions": [{
        "id": 3011,
        "name": "Jack Dorsey",
        "indices": [0, 11]
    }],
    "created_at": "2013-03-21T12:50:00Z",
    "updated_at": "2013-03-21T12:50:00Z"
}
```
