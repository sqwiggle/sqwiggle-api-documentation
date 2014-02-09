# Users

## Retrieve a User

Retrieves the details of any user that the token has access to. Supply a user ID and Sqwiggle will return 
the corresponding user profile information. You may pass 'me' instead of a user id to get information for
the current token.

### Request

<div class="request">
    <code class="http" title="HTTP">GET /users/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::User.find(id)</code>
</div>


## Update a User

Updates the specified user by setting the values of the parameters passed. Any parameters not provided 
will be left unchanged, unrecognised parameters will result in the request returning an error response.

### Request

<div class="request">
    <code class="http" title="HTTP">PUT /users/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::User.find(id)</code>
</div>

### Parameters

<table>
    <tr>
        <td>name</td>
        <td>optional</td>
        <td>The users full display name</td>
    </tr>
    <tr>
        <td>email</td>
        <td>optional</td>
        <td>The users email address</td>
    </tr>
    <tr>
        <td>time_zone</td>
        <td>optional</td>
        <td>The users time zone (in rails format)</td>
    </tr>
    <tr>
        <td>avatar</td>
        <td>optional</td>
        <td>A URL pointing to the users avatar, this must reside on Sqwiggle's servers</td>
    </tr>
    <tr>
        <td>status</td>
        <td>optional</td>
        <td>Status enum may be set to one of 'busy', 'available' or 'offline'</td>
    </tr>
    <tr>
        <td>message</td>
        <td>optional</td>
        <td>A custom message which will be displayed to other users</td>
    </tr>
</table>

## Remove a User

This endpoint is not currently accessible by API clients.


## List all Users

Returns a list of all users in the current organization. The users are returned in sorted alphabetical order 
by default.

### Request

<div class="request">
    <code class="http" title="HTTP">GET /users</code>
    <code class="ruby" title="Ruby">Sqwiggle::User.all</code>
</div>

### Parameters

<table>
    <tr>
        <td>page</td>
        <td>optional</td>
        <td>For paginating through large numbers of users, the page of results to retrieve</td>
    </tr>
    <tr>
        <td>limit</td>
        <td>optional</td>
        <td>The number of users to return (between 1-100)</td>
    </tr>
</table>

