# Attachments

## Retrieve an Attachment

Retrieves the details of a message attachment. There are many different types of attachments and each type may return different fields in the response.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /attachments/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Attachment.find(id)</code>
    <code class="js" title="Node.js">client.attachments.find(id, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the attachment to retrieve</td>
    </tr>
</table>


## Update an Attachment

Updates the specified attachment by setting the values of the parameters passed. Note that changes made via the API will be immediately reflected in the interface of all connected clients.

### Request
<div class="request">
    <code class="http" title="HTTP">PUT /attachments/:id</code>
    <code class="ruby" title="Ruby">
a = Sqwiggle::Attachment.find(id)
a.title = "My new attachment title"
a.save
    </code>
    <code class="js" title="Node.js">client.attachments.update(id, {title: "My new attachment title"}, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the attachment to update</td>
    </tr>
    <tr>
        <td>title</td>
        <td>optional</td>
        <td>A title for the attachment, for example a filename or webpage title</td>
    </tr>
    <tr>
        <td>description</td>
        <td>optional</td>
        <td>A description of the attachment, for example a web page summary</td>
    </tr>
    <tr>
        <td>url</td>
        <td>optional</td>
        <td>The URL of the attachment, this may not reside on Sqwiggle's servers</td>
    </tr>
    <tr>
        <td>image</td>
        <td>optional</td>
        <td>The URL for an optional preview image</td>
    </tr>
    <tr>
        <td>status</td>
        <td>optional</td>
        <td>If an upload, this string denotes whether the upload is 'pending' or 'uploaded'. (Null if not an upload E.G. a link attachment)</td>
    </tr>
</table>


## Remove an Attachment

Removes the specified attachment from the parent message. If this is the only attachment in the message then the parent message will
also be removed.

### Request
<div class="request">
    <code class="http" title="HTTP">DELETE /attachments/:id</code>
    <code class="ruby" title="Ruby">
a = Sqwiggle::Attachment.find(id)
a.delete
    </code>
    <code class="js" title="Node.js">client.attachments.delete(id, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the attachment to remove</td>
    </tr>
</table>


## List all Attachments

Returns a list of all attachments in the current organization. The attachments are returned in reverse date order 
by default.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /attachments</code>
    <code class="ruby" title="Ruby">Sqwiggle::Attachment.all(page: 1, limit: 100)</code>
    <code class="js" title="Node.js">client.attachments.index({page: 1, limit: 100}, function(err, resp){});</code>
</div>


### Parameters
<table>
    <tr>
        <td>page</td>
        <td>optional</td>
        <td>For paginating through large numbers of attachments, the page of results to retrieve</td>
    </tr>
    <tr>
        <td>limit</td>
        <td>optional</td>
        <td>The number of attachments to return (between 1-100)</td>
    </tr>
</table>
