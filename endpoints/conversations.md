# Conversations

## <a name="retrieveaconversation"></a>Retrieve a Conversation

Retrieves the details of a specific conversation provided it is accessible via the provided token.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /conversations/:id</code>
    <code class="ruby" title="Ruby">Sqwiggle::Conversation.find(id)</code>
    <code class="js" title="Node.js">client.conversations.find(id, function(err, resp){});</code>
</div>

### Parameters
<table>
    <tr>
        <td>id</td>
        <td>required</td>
        <td>ID of the conversation object to retrieve</td>
    </tr>
</table>

## <a name="listallconversations"></a>List all Conversations

Returns a list of all conversations within the organization associated with the provided token. This includes both finished and ongoing. 

### Request
<div class="request">
    <code class="http" title="HTTP">GET /conversations</code>
    <code class="ruby" title="Ruby">Sqwiggle::Conversation.all(page: 1, limit: 100)</code>
    <code class="js" title="Node.js">client.conversations.list({page: 1, limit: 100}, function(err, resp));</code>
</div>


### Parameters
<table>
    <tr>
        <td>page</td>
        <td>optional</td>
        <td>For paginating through large numbers of conversations, the page of results to retrieve</td>
    </tr>
    <tr>
        <td>limit</td>
        <td>optional</td>
        <td>The number of conversations to return (between 1-100)</td>
    </tr>
</table>
