# Content Click

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "content_click",
  "detailed_event": "Content Click",
    "event_data": {
        "link_text": "<link_text>",
        "link_url": "<link_url>",
        "topics": "<topics>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.link_text|string|Text of the link clicked|Article name, "Sign Up"|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.example.com|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\)|Branding,Managing money,Website design|||||||
|user_data.user_id|string|The hashed email of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||

## Attached Notes

<p>Within the Info Hub, please limit the number of "topics" sent in the string to 3. There is a character limit of 100 characters, and we prefer this to be limited within the dataLayer.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
