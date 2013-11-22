# Users

## Create a User

This endpoint is not currently accessible by clients.


## Retrieve a User

Retrieves the details of any user that the token has access to. Supply a user ID and Sqwiggle will return 
the corresponding user profile information. You may pass 'me' instead of a user id to get information for
the current token.

<dl>
  <dt>id</dt>
  <dd>required</dd>
</dl>


## Update a User

Updates the specified user by setting the values of the parameters passed. Any parameters not provided 
will be left unchanged, unrecognised parameters will result in the request returning an error response.

<dl>
  <dt>id</dt>
  <dd>required</dd>
  <dt>name</dt>
  <dd>optional
  The users full display name</dd>
  <dt>email</dt>
  <dd>optional</dd>
  <dt>time_zone</dt>
  <dd>optional</dd>
  <dt>avatar</dt>
  <dd>optional</dd>
  <dt>status</dt>
  <dd>optional
  Status may be set to one of 'busy' or 'available'</dd>
  <dt>message</dt>
  <dd>optional
  A message which will be displayed to other users</dd>
</dl>


## Remove a User

This endpoint is not currently accessible by clients.


## List all Users

Returns a list of all users in the current organization. The users are returned in sorted alphabetical order 
by default.

<dl>
  <dt>page</dt>
  <dd>optional</dd>
  <dt>limit</dt>
  <dd>optional</dd>
</dl>


## Ping a User

You can 'ping' another user to get their attention. This is usually used when the other user is set to busy, 
but could be used at other times. The client name and image will appear in the ping notification.

<dl>
  <dt>id</dt>
  <dd>required</dd>
</dl>
