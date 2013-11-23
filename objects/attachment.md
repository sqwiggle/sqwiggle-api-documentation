# Attachment
An attachment object is a piece of media that belongs to a message, it may represent a link, image, video, file upload or more. We often add new attachment types based on demand so it is important to filter using the type parameter.

## Attributes
<table>
    <tr>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <td>type</td>
        <td>enum</td>
        <td>image, link, file, twitter_status, twitter_user, video, code, gist</td>
    </tr>
    <tr>
        <td>title</td>
        <td>string</td>
        <td>A title for the attachment, for example a filename or webpage title</td>
    </tr>
    <tr>
        <td>description</td>
        <td>string</td>
        <td>A description of the attachment, for example a web page summary</td>
    </tr>
    <tr>
        <td>image</td>
        <td>string</td>
        <td>URL of an image representing the attachment, this may not reside on Sqwiggle's servers</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>datetime</td>
        <td>The time that this message was created</td>
    </tr>
    <tr>
        <td>updated_at</td>
        <td>datetime</td>
        <td>The time that this message was last updated or edited</td>
    </tr>
</table>


## Example

```
{
    "id": 1234,
    "type": "link",
    "title": "Google",
    "image": "https://www.google.com/images/google_favicon_128.png",
    "description": "The worlds favorite search engine",
    "url": "https://www.google.com",
    "created_at": "2013-04-01T11:54:00Z",
    "updated_at": "2013-04-01T11:55:02Z"
}
```
