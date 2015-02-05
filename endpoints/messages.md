# Messages

## <a name="createamessage"></a>Create a Message

Create a new message in a chat stream, new messages will be pushed to connected clients. If a link is detected in the message then it will be parsed and appropriate attachments will be automatically generated - for example a link to a youtube video would generate an attachment of type 'Video' with corresponding fields.

### Request
<div class="request">
    <code class="http" title="HTTP">POST /messages</code>
    <code class="ruby" title="Ruby">Sqwiggle::Message.new(text: "Sqwiggle is pretty neat")</code>
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
        <td>stream_id</td>
        <td>required</td>
        <td>The id of the stream to post the message into</td>
    </tr>
</table>

### Mentions

You can also "@mention" a user by including a specially formatted string in the message text. The format is illustrated below, simply replace user_name and user_id with a given users name and id.

<code>
@(<em>user_name</em>)[user:<em>user_id</em>]
</code>



## <a name="retrieveamessage"></a>Retrieve a Message

Retrieves the details of a message and any nested attachments.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /messages/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Message.find(id)</code>
    <code class="js" title="Node.js">client.messages.find(id, function(err, resp){})</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the message to retrieve</td>
    </tr>
</table>


## <a name="updateamessage"></a>Update a Message

Updates the specified message by setting the values of the parameters passed. Note that changes made via the API will be immediately reflected in the interface of all connected clients.

### Request
<div class="request">
    <code class="http" title="HTTP">PUT /messages/:id</code>
    <code class="ruby" title="Ruby">
m = Sqwiggle::Message.find(id)
m.text = "I edited this message"
m.save
    </code>
    <code class="js" title="Node.js">client.messages.update(id, {text: "I edited this messsage"}, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the message to update</td>
    </tr>
    <tr>
        <td>text</td>
        <td>required</td>
        <td>The new text for the message</td>
    </tr>
</table>


## <a name="removeamessage"></a>Remove a Message

Removes the specified message from the stream. So that conversation flow is preserved the message will be replaced with a _"This message has been removed"_ note in the stream.

### Request
<div class="request">
    <code class="http" title="HTTP">DELETE /messages/:id</code>
    <code class="ruby" title="Ruby">
m = Sqwiggle::Message.find(id)
m.delete
    </code>
    <code class="js" title="Node.js">client.messages.delete(id, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the message to remove</td>
    </tr>
</table>


## <a name="listallmessages"></a>List all Messages

Returns all messages in the current organization across all streams. The messages are returned in reverse date order 
by default.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /messages</code>
    <code class="ruby" title="Ruby">Sqwiggle::Message.all(page: 1, limit: 100)</code>
    <code class="js" title="Node.js">client.messages.index({page: 1, limit: 100}, function(err, resp){});</code>
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

