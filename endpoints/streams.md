# Streams

## Create a Stream

Streams can be created from the app interfaces, or programatically via the API. We currently have no restrictions on the number of chat streams you can create within an organization.

### Request
<div class="request">
    <code class="http" title="HTTP">POST /streams</code>
    <code class="ruby" title="Ruby">Sqwiggle::Room.create</code>
    <code class="js" title="Node.js">client.rooms.create({name: 'Support Team'}, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>name</td>
        <td>required</td>
        <td>Display name of the stream</td>
    </tr>
</table>


## Retrieve a Stream

Retrieves the details of any stream that the token has access to. Supply an ID and Sqwiggle will return 
the corresponding chat stream object.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /streams/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Room.find(id)</code>
    <code class="js" title="Node.js">client.rooms.find(id, function(err, resp){});</code>
</div>


## Update a Stream

Updates the specified stream by setting the values of the parameters passed. At this time the only parameter
that can be changed is the name, paths will be automatically generated.

### Request

<div class="request">
    <code class="http" title="HTTP">PUT /streams/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Room.find(id).update(params)</code>
    <code class="js" title="Node.js">client.rooms.update(id, {name: 'More Fun Room'}, function(err, resp){});</code>
</div>

### Parameters

<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the stream object to update</td>
    </tr>
    <tr>
        <td>name</td>
        <td>optional</td>
        <td>The stream display name</td>
    </tr>
</table>


## Remove a Stream

Removes the chat stream from the organisation.

### Request 

<div class="request">
    <code class="http" title="HTTP">DELETE /streams/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Room.find(id).delete</code>
    <code class="js" title="Node.js">client.rooms.delete(id, function(err, resp){});</code>
</div>


## List all Streams

Returns a list of all streams in the current organization. The streams are returned in sorted alphabetical order 
by default.

### Request 

<div class="request">
    <code class="http" title="HTTP">GET /streams</code>
    <code class="ruby" title="Ruby">Sqwiggle::Room.all</code>
    <code class="js" title="Node.js">client.rooms.index({page: 1, limit: 100}, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>page</td>
        <td>optional</td>
        <td>For paginating through large numbers of streams, the page of results to retrieve</td>
    </tr>
    <tr>
        <td>limit</td>
        <td>optional</td>
        <td>The number of streams to return (between 1-100)</td>
    </tr>
</table>
