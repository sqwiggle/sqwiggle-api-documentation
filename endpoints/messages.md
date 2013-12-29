# Messages

## Create a Message

Create a new message in an individual room, new messages will be pushed to connected clients. If a link is detected in the message then it will be parsed and appropriate attachments will be automatically generated - for example a link to a youtube video would generate an attachment of type 'Video' with corresponding fields.

### Request
<div class="request">
    <code class="http" title="HTTP">POST /messages</code>
    <code class="ruby" title="Ruby">Sqwiggle::Message.new(message: "Sqwiggle is pretty neat")</code>
</div>

### Parameters
<table>
    <tr>
        <td>text</td>
        <td>required</td>
        <td>The text of the message</td>
    </tr>
    <tr>
        <td>format</td>
        <td>optional</td>
        <td>Set this parameter to 'html' to allow a subset of HTML tags in the message</td>
    </tr>
    <tr>
        <td>parse</td>
        <td>optional</td>
        <td>Whether links in the message should be converted to rich attachments</td>
    </tr>
    <tr>
        <td>room_id</td>
        <td>required</td>
        <td>The id of the room to post the message to</td>
    </tr>
</table>


## Retrieve a Message

Retrieves the details of a message and any nested attachments.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /messages/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Message.find(id)</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the message to retrieve</td>
    </tr>
</table>


## Update a Message

Updates the specified message by setting the values of the parameters passed. Note that changes made via the API will be immediately reflected in the interface of all connected clients.

### Request
<div class="request">
    <code class="http" title="HTTP">PUT /messages/:id</code>
    <code class="ruby" title="Ruby">
m = Sqwiggle::Message.find(id)
m.message = "I edited this message"
m.save
    </code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the message to update</td>
    </tr>
    <tr>
        <td>message</td>
        <td>required</td>
        <td>The new text for the message</td>
    </tr>
</table>


## Remove a Message

Removes the specified message from the room, so that conversation flow is preserved the message will be replaced with a _"This message has been removed"_ note in the stream.

### Request
<div class="request">
    <code class="http" title="HTTP">DELETE /messages/:id</code>
    <code class="ruby" title="Ruby">
m = Sqwiggle::Message.find(id)
m.delete
    </code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the message to remove</td>
    </tr>
</table>


## List all Messages

Returns all messages in the current organization across all rooms. The messages are returned in reverse date order 
by default.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /messages</code>
    <code class="ruby" title="Ruby">Sqwiggle::Message.all(page: 1, limit: 100)</code>
</div>


### Parameters
<table>
    <tr>
        <td>page</td>
        <td>optional</td>
        <td>For paginating through large numbers of messages, the page of results to retrieve</td>
    </tr>
    <tr>
        <td>limit</td>
        <td>optional</td>
        <td>The number of messages to return (between 1-100)</td>
    </tr>
</table>

