All requests to the API must be made over HTTPS. You can authenticate with the Sqwiggle API 
using an access token, which is passed via HTTP Basic Authentication and goes in the username 
field. A dummy password, such as X, goes in the password field. 

An example request using CURL would be in the form of:

`$ curl -u wXcYlkkTo3reEJ:X https://api.sqwiggle.com/users/me`
