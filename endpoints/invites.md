# Invites

## Create an Invite

When an invite is created an email is automatically sent to the recipients address asking them to join your organization. Please bear this in mind when creating invites for test purposes, abuse of this API may result 
in your account becoming blocked. 

### Request
<div class="request">
    <code class="http" title="HTTP">POST /invites</code>
    <code class="ruby" title="Ruby">Sqwiggle::Invites.new(email: 'example@example.org')</code>
</div>

### Parameters
<table>
    <tr>
        <td>email</td>
        <td>required</td>
        <td>Email address that will receive the invite</td>
    </tr>
</table>


## Retrieve an Invite

Retrieves the details of any invite that has been previously created. Supply an invite ID to get details of
the invite.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /invites/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Invites.find(id)</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the invite object to retrieve</td>
    </tr>
</table>


## Remove an Invite

Removes the specified invite from the organization. This will result in the invite no longer working should the recipient click on the link contained in the invite email.

### Request
<div class="request">
    <code class="http" title="HTTP">DELETE /invites/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Invites.destroy(id)</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the invite object to remove</td>
    </tr>
</table>


## List all Invites

Returns a list of all outstanging invites in the current organization.
by default.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /invites</code>
    <code class="ruby" title="Ruby">Sqwiggle::Invites.all(page: 1, limit: 100)</code>
</div>

### Parameters
<table>
    <tr>
        <td>page</td>
        <td>optional</td>
        <td>For paginating through large numbers of invites, the page of results to retrieve</td>
    </tr>
    <tr>
        <td>limit</td>
        <td>optional</td>
        <td>The number of invites to return (between 1-100)</td>
    </tr>
</table>