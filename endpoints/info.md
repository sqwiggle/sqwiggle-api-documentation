# Info
General information in this namespace is generally used by the official Sqwiggle clients in order to function and update themselves.

## Retrieve Configuration
Returns configuration information for Sqwiggle clients, such as where to store file uploads, limits, ice servers and other misc details that are required.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /info/configuration</code>
    <code class="ruby" title="Ruby">Sqwiggle::Info.configuration</code>
</div>

## Retrieve Versions
Returns the current versions of the official Sqwiggle clients across all platforms, this allows apps to auto-update when a new version is available.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /info/versions</code>
    <code class="ruby" title="Ruby">Sqwiggle::Info.versions</code>
</div>

## Retrieve All
Returns the configuration and version details in a single request.

### Request
<div class="request">
    <code class="http" title="HTTP">GET /info</code>
    <code class="ruby" title="Ruby">Sqwiggle::Info</code>
</div>