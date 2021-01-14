## Language Detection 

> Request example - `POST fromURL`...


```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/text/languagedetection/fromURL?access_token=YOUR_ACCESS_TOKEN"
```
> ... and response body (200/JSON):

```json
{
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "lang-ext": "English", 
  "lang": "en"
}
```


> Request example - `POST fromText`...

```shell
curl --ssl-reqd --request POST --data text="The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]" "https://api.yonderlabs.com/1.0/text/languagedetection/fromText?access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):

```json
{
  "url": null, 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "lang-ext": "English", 
  "lang": "en"
}
```








**Recognize the language of your text (over 50 languages)**

This service recognizes the language a document were written in, including English, Italian, Spanish, French, German, and other main languages.
Allowed input sources are: text content contained in an URL ("from URL") or just simple text ("from text").


### Language Extraction - `POST fromURL`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the text document | use [url-encoding](http://www.url-encode-decode.com/)|

Parameter | Type | Description | 
--------- | ------- | ----------- | 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.

### Language Extraction - `POST fromText`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
text | string, required | the text to be classified | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|

Parameter | Type | Description | 
--------- | ------- | ----------- | 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication!
</aside>

      