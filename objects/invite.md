# Invite
An invite represents an email invitation to join an organization.

## Attributes
<table>
    <tr>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <td>from_id</td>
        <td>integer</td>
        <td>Id of the user that created the invite</td>
    </tr>
    <tr>
        <td>email</td>
        <td>string</td>
        <td>The email address that this invite was sent to</td>
    </tr>
    <tr>
        <td>avatar</td>
        <td>string</td>
        <td>URL to a static avatar representing the email address</td>
    </tr>
    <tr>
        <td>url</td>
        <td>string</td>
        <td>URL to redeem the invite</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time that this invite was created</td>
    </tr>
</table>


## Example

```
{
    "id": 1234,
    "from_id": 5678,
    "email": "invited@example.com",
    "avatar: "",
    "url": "https://www.sqwiggle.com/signup/hG60KLmf3mfL11",
    "created_at": "2013-10-11T03:00:00Z"
}
```
