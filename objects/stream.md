# Stream
A stream represents a single group chat in which messages can be exchanged within Sqwiggle.

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
        <td>Id of the user that created this stream</td>
    </tr>
    <tr>
        <td>name</td>
        <td>string</td>
        <td>The full stream name</td>
    </tr>
    <tr>
        <td>path</td>
        <td>string</td>
        <td>The path to access stream in the web app, eg app.sqwiggle.com/:path</td>
    </tr>
    <tr>
        <td>icon</td>
        <td>string</td>
        <td>An icon representing the stream</td>
    </tr>
    <tr>
        <td>icon_color</td>
        <td>string</td>
        <td>A color representing the stream in hex format (eg: #121212)</td>
    </tr>
    <tr>
        <td>subscribed</td>
        <td>boolean</td>
        <td>Whether the user receives notifications for this stream</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time that this stream was created</td>
    </tr>
</table>

## Example

    {   
        "id": 1234,
        "user_id": 5678,
        "name": "Engineering",
        "path": "engineering",
        "subscribed": true,
        "created_at": "2013-04-01T06:00:38Z"
    }
