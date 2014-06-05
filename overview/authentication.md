# Authentication

All requests to the API must be made over HTTPS. You can authenticate with the Sqwiggle API 
using an access token, which is passed via HTTP Basic Authentication and goes in the username 
field. The client token acts as both identifier and verification, with the password not being used. It is common to pass X for the password.

An example request using CURL would be in the form of:

`$ curl -u wXcYlkkTo3reEJ:X https://api.sqwiggle.com/users/me`


## Roles

Clients can have one of three roles, these offer a predefined set of access permissions.

### Stream
Stream clients have access to read and write messages to any stream in the company, they can also read and write associated attachments. You should use this role for things like our GitHub integration or any other service that simply pushes into the chat stream. 

### Standard
Standard clients have much the same permissions as a Sqwiggle user, they may read organizations, users, messages etc and write records that the user has access to. This is enough for almost any integration you might want to create. 

**Note:** If you are creating an API client for use with [Zapier](https://www.zapier.com) the standard permissions **must** be used.

### Admin
Admin clients include all of the above permissions and also have ability to update the organization and any user within it. These tokens should be used with care.
