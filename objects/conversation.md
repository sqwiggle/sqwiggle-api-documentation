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
        <td>status</td>
        <td>enum</td>
        <td>open, closed</td>
    </tr>
    <tr>
        <td>duration</td>
        <td>integer</td>
        <td>The number of seconds this conversation lasted, or if open has been ongoing.</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time this conversation was started</td>
    </tr>
    <tr>
        <td>participating</td>
        <td>list</td>
        <td>A list of User objects that are currently participating in the conversation</td>
    </tr>
    <tr>
        <td>participated</td>
        <td>list</td>
        <td>A list of User objects that have been and or are currently in the conversation</td>
    </tr>
</table>

## Example

    {   
        "id": 1234,
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
        "participated": [{
            "id": 3456,
            "name": "Elon Musk"
            ...
        }]
    }
