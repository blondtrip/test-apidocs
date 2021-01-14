## Concept Tagging

> Request example - `POST fromURL`...



```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/text/concepttagging/fromURL?limit=8&access_token=YOUR_ACCESS_TOKEN"
```


> ... and response body (200/JSON):

```json
{
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "limit": 8, 
  "tags": [
    "disasters and accidents", 
    "mh370", 
    "atsb", 
    "sumisha naidu", 
    "martin dolan", 
    "malaysia",
    "search",
    "area"
  ]
}
```

> Request example  - `POST fromText`...


```shell
curl --ssl-reqd --request POST --data text="The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]." "https://api.yonderlabs.com/1.0/text/concepttagging/fromText?limit=8&access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):

```json
{
  "url": null, 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
 "limit": 8, 
  "tags": [
    "disasters and accidents", 
    "mh370", 
    "atsb", 
    "sumisha naidu", 
    "martin dolan", 
    "malaysia",
    "search",
    "area"
  ]
}
```








**Generate high-level semantic tags for your text document**

Concept tags are a limited and meaningful set of highly relevant named entities and important keywords related to facts, events, and relations found in your text.
It is also possible to include custom whitelists and blacklists of concept tags upon request.
Allowed input sources are: text content contained in an URL ("from URL") or just simple text ("from text").


### Concept Tagging - `POST fromURL`



Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the text document | use [url-encoding](http://www.url-encode-decode.com/)|


Parameter | Type | Description | Value |
--------- | ------- | ----------- | ----- |
limit | number, optional | max # of relevant tags to be returned, in decreasing order of relevance | 1, 2, ..., 10 (default), etc. |
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.

### Concept Tagging - `POST fromText`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
text | string, required | the text to be classified | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|


Parameter | Type | Description | Value |
--------- | ------- | ----------- | ----- |
limit | number, optional | max # of relevant tags to be returned, in decreasing order of relevance | 1, 2, ..., 10 (default), etc. |
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.


<aside class="success">
Remember — insert your credentials for authentication!
</aside>





