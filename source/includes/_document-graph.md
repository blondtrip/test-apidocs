## Document Graph 


> Request example to "Create a Document Graph" - `POST`...

```shell
curl --ssl-reqd --include --request POST "https://api.yonderlabs.com/1.0/textcollection/documentgraph?collection_name=goofy&access_token=YOUR_ACCESS_TOKEN"
```
>... and response header and body (202 "ACCEPTED"):

```
HTTP/1.1 202 ACCEPTED
Server: nginx/1.4.6 (Ubuntu)
Date: Thu, 26 Oct 2017 10:50:27 GMT
Content-Type: application/json
Content-Length: 157
Connection: keep-alive
API-instance: instance01
```
```json
{
  "task_type": "DocumentGraphAPI", 
  "collection-name": "goofy", 
  "task_id": "a4e31278-4432-43da-8fbf-1b21562d02f9", 
  "task_status": "PENDING"
}
```

> Request example to "Get results from Document Graph" - `GET`...

```shell
curl --ssl-reqd --header "API-instance: instance01" --request GET "https://api.yonderlabs.com/1.0/textcollection/documentgraph?task_id=e92dff8f-29ca-4286-9876-68d965f4a066&access_token=YOUR_ACCESS_TOKEN"
```


>... and response body, case 1) SUCCESS, i.e. the task is over:

```json
{
  "task_error": null, 
  "task_type": "DocumentGraphAPI", 
  "task_id": "a4e31278-4432-43da-8fbf-1b21562d02f9", 
  "task_result": {
    "timestamp": "2015-12-29 16:28:06.517297", 
    "graph_list": [
      {
        "id": "5661ce38b1f53961fbb5ba8f", 
        "similar_documents": [
          {
            "id": "5661ce38b1f53961fbb5ba90", 
            "score": 0.2182018253178482
          }, 
          {
            "id": "5661ce38b1f53961fbb5bb43", 
            "score": 0.20725070321790517
          }
        ]
      }, 
      {
        "id": "5661ce38b1f53961fbb5bac7", 
        "similar_documents": [
          {
            "id": "5661ce38b1f53961fbb5bb78", 
            "score": 0.25007882768872314
          }, 
          {
            "id": "5661ce38b1f53961fbb5ba2d", 
            "score": 0.20836793197293701
          }, 
          {
            "id": "5661ce38b1f53961fbb5bb75", 
            "score": 0.1719251614907218
          }
        ]
      }
    ]
  }, 
  "collection_name": "goofy", 
  "task_status": "SUCCESS"
}
```


>... and response body, case 2) STARTED (the task has started, but it is not over):

```json
{
  "task_type": "DocumentGraphAPI", 
  "task_id": "e92dff8f-29ca-4286-9876-68d965f4a066", 
  "task_status": "STARTED"
}
```

>... and response body, case 3) PENDING (the task is still pending):

```json
{
  "task_type": "DocumentGraphAPI", 
  "task_id": "e92dff8f-29ca-4286-9876-68d965f4a066", 
  "task_status": "PENDING"
}
```



**Compute all document similarities in your Text Collection**

This API analyzes a collection of texts and returns all document cross-similarities.


<aside class="notice">
Depending on the size of the Text Collection, this service might take up to few minutes to provide a full answer. 
</aside>

### Create a Document Graph - `POST`

This API allows you to launch the task which computes document cross-similarities on all items contained in a Text Collection.
As detailed in the right panel, as an immediate response to this API, you will get a `202` answer ("ACCEPTED") containing a task identifier `task_id` to be used later in the `GET` call. 

Please notice that the `--include` in the `POST` call displays the response header, which includes the `API-instance` field. The value of `API-instance` field (e.g. `instance01`) must be included later in the following `GET` call.


Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection from which to build a Document Graph | 
access_token | string, required | your access token (40 digits) |


### Get results from Document Graph - `GET`

This API allows you to retrieve computed document cross-similarities on all items contained in a Text Collection.
Please notice that the value of the `API-instance` field shown in the response header of the previous `POST` call (e.g. `instance01`) must be included in the `GET` call after the option `--header`, as detailed in the right panel.

Parameter | Type | Description | 
--------- | ------- | ----------- | 
task_id | string, required | the identifier of the created Document Graph task| 
access_token | string, required | your access token (40 digits) |

If results are ready (i.e. document similarities have been computed) you will get a `200` answer ("SUCCESS") and the resulting ouput, as detailed in the right panel (notice that only documents whose list of similar ones is not empty are reported).
If the process is still ongoing you will get an adequate status code answer ("STARTED" or "PENDING") meaning that you have to try again a bit later with another `GET` call. 

<aside class="notice">
In case of SUCCESS, results are promptly deleted afterwards, i.e. performing another GET on the same task_id will return no results.
</aside>

<aside class="success">
Remember — insert your credentials for authentication!
</aside>
