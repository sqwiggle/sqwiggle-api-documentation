# Conversation
A conversation object represents an ephemeral media connection between two or more people.

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
        <td>The room that this conversation took place in</td>
    </tr>
    <tr>
        <td>status</td>
        <td>enum</td>
        <td>open, closed</td>
    </tr>
    <tr>
        <td>participating</td>
        <td>list</td>
        <td>A list of User objects that are currently participating in the conversation</td>
    </tr>
    <tr>
        <td>users</td>
        <td>list</td>
        <td>A list of User objects that have been and or are currently in the conversation</td>
    </tr>
</table>

## Example

    {   
        "id": 1234,
        "room_id": 5678,
        "status": "open",
        "participating": [{
            "id": 3456,
            "name": "Elon Musk"
            ...
        },{
            "id": 9834,
            "name": "Bill Gates"
            ...
        }],
        "users": [{
            "id": 3456,
            "name": "Elon Musk"
            ...
        }]
    }
