# Error
An error object represents a user or server error and is returned with all non 2xx response codes.

## Attributes
<table>
    <tr>
        <td>type</td>
        <td>enum</td>
        <td>For a list of possible error types see the errors overview</td>
    </tr>
    <tr>
        <td>message</td>
        <td>string</td>
        <td>A human readable message for display to the end user</td>
    </tr>
    <tr>
        <td>details</td>
        <td>string</td>
        <td>Further error details useful for developer debugging. Should not be displayed to the end user.</td>
    </tr>
    <tr>
        <td>param</td>
        <td>string</td>
        <td>If the error is tied to a specific parameter it will be reflected here</td>
    </tr>
</table>


## Example

    {
        "type": "authentication",
        "message": "Sorry, your account could not be authenticated",
        "details": "Did you provide an auth_token? For details on how to authorize with the API 
        please see our documentation here: https://www.sqwiggle.com/docs/overview/authentication",
        "param": ""
    }
