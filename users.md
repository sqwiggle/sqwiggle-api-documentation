# Users

## Create a User

This endpoint is not currently accessible by clients.


## Retrieve a User

Retrieves the details of any user that the token has access to. Supply a user ID and Sqwiggle will return 
the corresponding user profile information. You may pass 'me' instead of a user id to get information for
the current token.


## Update a User

Updates the specified user by setting the values of the parameters passed. Any parameters not provided 
will be left unchanged, unrecognised parameters will result in the request returning an error response.


## Remove a User

This endpoint is not currently accessible by clients.


## List all Users

Returns a list of all users in the current organization. The users are returned in sorted alphabetical order 
by default.


## Ping a User

You can 'ping' another user to get their attention. This is usually used when the other user is set to busy, 
but could be used at other times. The client name and image will appear in the ping notification.
