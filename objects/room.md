# Room
A room represents a space in Sqwiggle where users can exchange messages and conduct conversations.

## Attributes
<table>
    <tr>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <td>user_id</td>
        <td>integer</td>
        <td>Id of the user that created this room</td>
    </tr>
    <tr>
        <td>name</td>
        <td>string</td>
        <td>The full room name</td>
    </tr>
    <tr>
        <td>path</td>
        <td>string</td>
        <td>The path to access room in the web app, eg sqwiggle.com/:company/:path</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time that this room was created</td>
    </tr>
</table>

## Example

    {   
        "id": 1234,
        "user_id": 5678,
        "name": "Engineering",
        "path": "engineering",
        "created_at": "2013-04-01T06:00:38Z"
    }
