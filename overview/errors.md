# Errors

We use standard HTTP status codes to communicate the success or failure of an API request. 
A code in the 200's indicates success, 400's indicates an error that resulted from the provided information 
(e.g. a required parameter was missing) and a 500 indicates that something went wrong on our end.

The response body will always be JSON and contain an Error object.

## Error Types

<table>
    <tr>
        <td>authentication</td>
        <td>An incorrect or invalid authentication token was supplied</td>
    </tr>
    <tr>
        <td>authorization</td>
        <td>The client does not have permission to perform the requested
        operation</td>
    </tr>
    <tr>
        <td>invalid_param</td>
        <td>One or more of the parameters provided were invalid</td>
    </tr>
    <tr>
        <td>unknown_param</td>
        <td>One or more of the parameters provided were not recognized</td>
    </tr>
    <tr>
        <td>limit_reached</td>
        <td>The request was made too fast, wait and try again</td>
    </tr>
    <tr>
        <td>validation</td>
        <td>One or more of the parameters didn't fulfill the validation.</td>
    </tr>
    <tr>
        <td>unknown</td>
        <td>Usually accompanies an unexpected server error, please get in touch.</td>
    </tr>
</table>
