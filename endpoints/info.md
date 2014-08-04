# Info
General information in this namespace is generally used by the official Sqwiggle clients in order to function and update themselves.

## Retrieve Configuration
Returns configuration information for Sqwiggle clients, such as where to store file uploads, limits, ice servers and other misc details that are required.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /info/configuration</code>
    <code class="ruby" title="Ruby">Sqwiggle::Info.configuration</code>
    <code class="js" title="Node.js">client.info.configuration(function(err, resp){});</code>
</div>

## Retrieve All
Returns the configuration and version details in a single request.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /info</code>
    <code class="ruby" title="Ruby">Sqwiggle::Info</code>
    <code class="js" title="Node.js">client.info.all(function(err, resp){});</code>
</div>
