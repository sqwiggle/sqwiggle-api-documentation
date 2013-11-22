# Organization
Every user belongs to an organization.

## Attributes
<table>
    <tr>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <td>name</td>
        <td>string</td>
        <td>The full organisation name</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time that this company was created</td>
    </tr>
    <tr>
        <td>path</td>
        <td>string</td>
        <td>The url path to access company on app, eg sqwiggle.com/:path</td>
    </tr>
    <tr>
        <td>billing</td>
        <td>hash</td>
        <td></td>
    </tr>
    <tr>
        <td>security</td>
        <td>hash</td>
        <td></td>
    </tr>
</table>

## Example
```
{   
    "id": 1234,
    "name": "Acme, Inc",
    "created_at": "2013-01-01T03:18:33Z",
    "billing: {
        "receipts": true,
        "email": "billing@acmeinc.com"
    },
    "security: {
        "media_accept": false,
        "domain_restrict": false,
        "domain_signup": true,
        "open_invites": true
    }
}
```
