# Organizations

## Retrieve an Organization

Retrieves the details of any organization that the token has access to. At this time each user can only belong to a single organization and all API requests are scoped by a single organization.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /organizations/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Organization.find(id)</code>
    <code class="js" title="Node.js">client.organizations.find(id, function(err, resp){})</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the organization object to retrieve</td>
    </tr>
</table>


## Update an Organization

Updates the specified organization by setting the values of the parameters passed. At this time the only parameter that can be changed is the organization name, paths will be automatically generated.

### Request
<div class="request">
    <code class="http" title="HTTP">PUT /organizations/:id</code>
    <code class="ruby" title="Ruby">
o = Sqwiggle::Organization.find(id)
o.name = "Acme, Inc"
o.save
    </code>
    <code class="js" title="Node.js">client.organizations.update(id, {name: 'Acme, Inc'}, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the organization object to update</td>
    </tr>
    <tr>
        <td>name</td>
        <td>optional</td>
        <td>The organizations name</td>
    </tr>
</table>


## List all Organizations

Returns a list of all organizations the current token has access to. At this time each user can only belong to a single organization and all API requests are scoped by a single organization.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /organizations</code>
    <code class="ruby" title="Ruby">Sqwiggle::Organization.all</code>
    <code class="ruby" title="Ruby">client.organizations.index(null, function(err, resp){});</code>
</div>

