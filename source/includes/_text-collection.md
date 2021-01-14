## Text Collection
> Request example to "Create a Text Collection" - `POST`...

```shell
curl --ssl-reqd --request POST "https://api.yonderlabs.com/1.0/textcollection/textcollection?collection_name=donald-duck&description=this-is-my-first-collection&access_token=YOUR_ACCESS_TOKEN"
```

>... and response body (200/JSON):

```json
{
  "type": "private", 
  "description": "this-is-my-first-collection", 
  "collection_name": "donald-duck", 
  "created": true
}
```



> Request example to "Get info from a Text Collection" - `GET`...


```shell
curl --ssl-reqd --request GET "https://api.yonderlabs.com/1.0/textcollection/textcollection?collection_name=donald-duck&access_token=YOUR_ACCESS_TOKEN"
```

>... and response body (200/JSON):

```json
{
  "count": 0, 
  "type": "private", 
  "description": "this-is-my-first-collection", 
  "collection_name": "donald-duck"
}
```


> Request example to "List all Text Collections" - `GET`...


```shell
curl --ssl-reqd --request GET "https://api.yonderlabs.com/1.0/textcollection/textcollection?access_token=YOUR_ACCESS_TOKEN"
```

>... and response body (200/JSON):

```json
{
  "collections": [
    {
      "count": 5, 
      "collection_name": "scrooge", 
      "type": "private", 
      "description": "This-is-my-first-collection."
    }, 
    {
      "count": 12, 
      "collection_name": "donald-duck", 
      "type": "private", 
      "description": "This-is-another-collection."
    }, 
    {
      "count": 0, 
      "collection_name": "daisy", 
      "type": "private", 
      "description": "Yet-another-text-collection."
    }
  ]
}
```





> Request example to "Delete a Text Collection" - `DELETE`...


```shell
curl --ssl-reqd --request DELETE "https://api.yonderlabs.com/1.0/textcollection/textcollection?collection_name=donald-duck&access_token=YOUR_ACCESS_TOKEN"
```

>... and response body (200/JSON):

```json
{
  "deleted": true, 
  "type": "private", 
  "description": "this-is-my-first-collection", 
  "collection_name": "donald-duck"
}
```




**Create, delete, and retrieve information from Text Collections**

This API allows you to create, delete, and get information from a single Text Collection, and list all existing Text Collections.


### Create a Text Collection - `POST`

This API allows you to create a new Text Collection:


Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection to be created | 
description | string, optional | a textual description of the Text Collection | 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.


### Get info from a Text Collection - `GET`

This API allows you to retrieve all information from a Text Collection:


Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection from which to retrieve information| 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.


### List all Text Collections - `GET`

This API allows you to retrieve information about all your existing Text Collections:


Parameter | Type | Description | 
--------- | ------- | ----------- | 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.


### Delete a Text Collection - `DELETE`

This API allows you to delete a Text Collection:



Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection to be deleted| 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication!
</aside>



