## Text Item



> Request example to "Create Text Item fromURL" - `POST fromURL`...

```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/textcollection/textitem/fromURL?collection_name=donald_duck&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "collection_name": "donald_duck", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "timestamp": "2015-12-29 16:28:06.517297", 
  "inserted_id": "5665a1e8b1f5391201471f86"
}
```


> Request example to "Create Text Item fromText"  - `POST fromText`...

```shell
curl --ssl-reqd --request POST --data text="The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]" "https://api.yonderlabs.com/1.0/textcollection/textitem/fromText?collection_name=donald_duck&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "url": null, 
  "collection_name": "donald_duck", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "timestamp": "2015-12-29 16:28:06.517297", 
  "inserted_id": "5665a1e8b1f5391201471f86"
}
```


> Request example to "Get info from Text Item"  - `GET`...

```shell
curl --ssl-reqd --request GET "https://api.yonderlabs.com/1.0/textcollection/textitem?collection_name=donald_duck&id=5665a1e8b1f5391201471f86&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "collection_name": "donald_duck", 
  "document": {
    "keywords": [
     {
      "score": 1,
      "name": "search"
     },
     {
      "score": 1,
      "name": "area"
     },
     {
      "score": 1,
      "name": "sq km"
     }
    ], 
   "entities": [
     {
      "info": null,
      "score": 1,
      "type": "Organization",
      "name": "MH370"
     },
     {
      "info": null,
      "score": 1,
      "type": "Organization",
      "name": "ATSB"
     },
     {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Chester",
        "description": "Chester (/ˈtʃɛstər/ CHESS-tər), is a city in Cheshire, England. Lying on the [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Chester"
     }
    ], 
    "timestamp": "2015-12-29 16:28:06.517297", 
    "_id": "5665a1e8b1f5391201471f86"
  }, 
  "fetched_id": "5665a1e8b1f5391201471f86"
}
```

> Request example to "List all Text Items"  - `GET`...

```shell
curl --ssl-reqd --request GET "https://api.yonderlabs.com/1.0/textcollection/textitem?collection_name=donald_duck&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "count": 12, 
  "ids": [
    "584aca4fb1f53952bc3a8781", 
    "584aca4fb1f53952bc3a8782", 
    "584aca50b1f53952c76440ee", 
    "584aca50b1f53952bc3a8783", 
    "584aca52b1f53952ba8cf07d", 
    "584aca51b1f53952c2845a4c", 
    "584aca51b1f53952c2845a4d", 
    "584aca51b1f53952c3672c0b", 
    "584aca51b1f53952c3672c0c", 
    "584aca52b1f53952c3672c0d", 
    "584aca52b1f53952c55577ea", 
    "584aca53b1f53952c3672c0e"
  ]
}
```


> Request example to "Modify Text Item fromURL"  - `PUT fromURL`...

```shell
curl --ssl-reqd --request PUT --data url=http%3A%2F%2Fwww.theguardian.com%2Fworld%2F2015%2Fnov%2F11%2Fgermany-spied-fbi-un-bodies-french-foreign-minister "https://api.yonderlabs.com/1.0/textcollection/textitem/fromText?collection_name=donald_duck&id=5665a1e8b1f5391201471f86&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "url": "http://www.theguardian.com/world/2015/nov/11/germany-spied-fbi-un-bodies-french-foreign-minister", 
  "collection_name": "donald_duck", 
  "modified_id": "5665a1e8b1f5391201471f86", 
  "timestamp": "2015-12-29 16:28:06.517297", 
  "text": "Germany's foreign intelligence service spied on targets including the French foreign minister, Laurent Fabius, the FBI and the UN Children's Fund, a media report said on Wednesday. The latest news report on the BND spy service fuels a debate in Germany about state surveillance kicked off by the revelations of the US whistleblower Edward Snowden [...]"
}
```


> Request example to "Modify Text Item fromText"  - `PUT fromText`...

```shell
curl --ssl-reqd --request PUT --data text="Germany's foreign intelligence service spied on targets including the French foreign minister, Laurent Fabius, the FBI and the UN Children's Fund, a media report said on Wednesday. The latest news report on the BND spy service fuels a debate in Germany about state surveillance kicked off by the revelations of the US whistleblower Edward Snowden [...]" "https://api.yonderlabs.com/1.0/textcollection/textitem/fromText?collection_name=donald_duck&id=5665a1e8b1f5391201471f86&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "url": null, 
  "collection_name": "donald_duck", 
  "modified_id": "5665a1e8b1f5391201471f86",
  "timestamp": "2015-12-29 16:28:06.517297",  
  "text": "Germany's foreign intelligence service spied on targets including the French foreign minister, Laurent Fabius, the FBI and the UN Children's Fund, a media report said on Wednesday. The latest news report on the BND spy service fuels a debate in Germany about state surveillance kicked off by the revelations of the US whistleblower Edward Snowden [...]"
}
```

> Request example to "Delete Text Item" - `DELETE`...

```shell
curl --ssl-reqd --request DELETE "https://api.yonderlabs.com/1.0/textcollection/textitem?collection_name=donald_duck&id=5665a1e8b1f5391201471f86&access_token=YOUR_ACCESS_TOKEN"
```
>... and response body (200/JSON):

```json
{
  "collection_name": "donald_duck", 
  "deleted_id": "5665a1e8b1f5391201471f86" 
 }
```






**Create, modify, delete, and retrieve info from Text Items in your Text Collections**

This API allows you to manage Text Items in your Text Collections (i.e. create, delete, modify, list). 


### Create Text Item - `POST fromURL` 

This API allows you to create a new Text Item from the text contained in a URL:

Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
collection_name | string, required | the name of the Text Collection where to insert the new Item | - |
url | string, required |the url of the text to be inserted as a new Item of the Text Collection | use [url-encoding](http://www.url-encode-decode.com/)|
access_token | string, required | your access token (40 digits) | - |

Examples of how-to-call the API and the related output are provided in the right panel.


### Create Text Item - `POST fromText` 

This API allows you to create a new Text Item inserting simple text:


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
collection_name | string, required | the name of the Text Collection where to insert the new Item | - |
text | string, required |the text to be inserted as a new Text Item | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|
access_token | string, required | your access token (40 digits) | - |

Examples of how-to-call the API and the related output are provided in the right panel.


### Get info from Text Item - `GET`

This API allows you to retrieve all information from a Text Item:


Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection which contains the Text Item| 
id | string, required |the ID of the text item|
access_token | string, required | your access token (40 digits) | 

Examples of how-to-call the API and the related output are provided in the right panel.

### List all Text Items - `GET`

This API allows you to list all Text Items in a Text Collection:


Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection which contains the Text Item| 
access_token | string, required | your access token (40 digits) | 

Examples of how-to-call the API and the related output are provided in the right panel.

### Change Text Item fromURL - `PUT fromURL`

This API allows you to change the text contained in a Text Item of a Text Collection:

Parameter | Type | Description |  Values |
--------- | ------- | ----------- | ------ |
collection_name | string, required | the name of the Text Collection where to change the item| - |
id | string, required |the ID of the text item| - |
url | string, required |the url of the text to be inserted | use [url-encoding](http://www.url-encode-decode.com/)|
access_token | string, required | your access token (40 digits) | - |

Examples of how-to-call the API and the related output are provided in the right panel.


### Change Text Item fromText - `PUT fromText`

This API allows you to change the text contained in a Text Item of a Text Collection:


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
collection_name | string, required | the name of the Text Collection where to change the item| - |
id | string, required |the ID of the text item| - |
text | string, required |the new text | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|
access_token | string, required | your access token (40 digits) | - |

Examples of how-to-call the API and the related output are provided in the right panel.

### Delete a Text Item - `DELETE`

This API allows you to delete a Text Item from a Text Collection:


Parameter | Type | Description 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection where to delete the Item| 
id | string, required |the ID of the Text Item to be deleted|
access_token | string, required | your access token (40 digits) | 

Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication!
</aside>



