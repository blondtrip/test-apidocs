## Document Clustering 


> Request example to "Cluster your text documents" - `POST`...

```shell
curl --ssl-reqd --include --request POST "https://api.yonderlabs.com/1.0/textcollection/documentclustering?collection_name=goofy&access_token=YOUR_ACCESS_TOKEN"
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
  "task_type": "DocumentClusteringAPI", 
  "collection-name": "goofy", 
  "task_id": "7284e228-a934-4a88-ac52-82764ed0b838", 
  "task_status": "PENDING"
}
```

> Request example to "Get results from Document Clustering" - `GET`...

```shell
curl --ssl-reqd --header "API-instance: instance01" --request GET "https://api.yonderlabs.com/1.0/textcollection/documentclustering?task_id=7284e228-a934-4a88-ac52-82764ed0b838&access_token=YOUR_ACCESS_TOKEN"
```


>... and response body, case 1) SUCCESS, i.e. the task is over:

```json
{
  "task_error": null, 
  "task_type": "DocumentClusteringAPI", 
  "task_id": "7284e228-a934-4a88-ac52-82764ed0b838", 
  "collection_name": "goofy", 
  "task_result": {
    "timestamp": "2017-02-20 10:12:20.047671", 
    "graph_clusters": [
      {
        "common_entities": [
          "Melania Trump", 
          "Melbourne", 
          "Fla", 
          "Donald Trump", 
          "Mussler", 
          "Florida", 
          "Melani", 
          "White House", 
          "Russian", 
          "U.S."
        ], 
        "common_tags": [
          "Melania Trump", 
          "president", 
          "rally", 
          "media", 
          "side", 
          "event", 
          "supporters", 
          "Melbourne", 
          "reporters", 
          "Donald Trump"
        ], 
        "ids": [
          "58aabf66b1f539056ab02d30", 
          "58aabfd1b1f539055b0aa27a"
        ], 
        "near_duplicates": [ ], 
        "common_keywords": [
          "president", 
          "rally", 
          "media", 
          "side", 
          "event", 
          "supporters", 
          "reporters", 
          "guests", 
          "attendance", 
          "way"
        ], 
        "size": 2
      }, 
      {
        "common_entities": [
          "USA TODAY Sports", 
          "NBA", 
          "Bob Donnan", 
          "James", 
          "Davis", 
          "Derick E. Hingle", 
          "Westbrook", 
          "Gerald Herbert", 
          "Western Conference", 
          "AP"
        ], 
        "common_tags": [
          "USA TODAY Sports", 
          "NBA", 
          "Bob Donnan", 
          "dunk", 
          "James", 
          "slam", 
          "Davis", 
          "contest", 
          "Derick E. Hingle", 
          "ball"
        ], 
        "ids": [
          "58aac083b1f53905654849f7", 
          "58aac0abb1f539056c74ef2f"
        ],
        "near_duplicates": [
          [ 
            "58aac083b1f53905654849f7", 
            "58aac0abb1f539056c74ef2f"
          ]
        ], 
        "common_keywords": [
          "dunk", 
          "slam", 
          "contest", 
          "ball", 
          "laugh", 
          "celebrities", 
          "guard", 
          "game", 
          "western conference", 
          "scores"
        ], 
        "size": 2
      }
    ]
  }, 
  "task_status": "SUCCESS"
}
```


>... and response body, case 2) STARTED (the task has started, but it is not over):

```json
{
  "task_type": "DocumentClusteringAPI", 
  "task_id": "7284e228-a934-4a88-ac52-82764ed0b838", 
  "task_status": "STARTED"
}
```

>... and response body, case 3) PENDING (the task is still pending):

```json
{
  "task_type": "DocumentClusteringAPI", 
  "task_id": "7284e228-a934-4a88-ac52-82764ed0b838", 
  "task_status": "PENDING"
}
```



**Cluster text documents in your Text Collection**

This API analyzes a collection of texts and clusters documents according to their similarities.


<aside class="notice">
Depending on the size of the Text Collection, this service might take up to few minutes to provide a full answer. 
</aside>

### Launch a Document Clustering - `POST`

This API allows you to launch the task which computes document clusters on all  the items contained in a Text Collection.
As detailed in the right panel, as an immediate response to this API, you will get a `202` answer ("ACCEPTED") containing a task identifier `task_id` to be used later in the `GET` call. 

Please notice that the `--include` in the `POST` call displays the response header, which includes the `API-instance` field. The value of `API-instance` field (e.g. `instance01`) must be included later in the following `GET` call.

Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection on which to lauch Document Clustering | 
access_token | string, required | your access token (40 digits) |


### Get results from Document Clustering - `GET`

This API allows you to retrieve computed document clusters contained in a Text Collection.
Please notice that the value of the `API-instance` field shown in the response header of the previous `POST` call (e.g. `instance01`) must be included in the `GET` call after the option `--header`, as detailed in the right panel.


Parameter | Type | Description | 
--------- | ------- | ----------- | 
task_id | string, required | the identifier of the created Document Clustering task| 
access_token | string, required | your access token (40 digits) |

If results are ready (i.e. document clusters have been computed) you will get a `200` answer ("SUCCESS") and the resulting ouput, as detailed in the right panel.
Please notice that, in case duplicates or near-duplicates are found, these are listed in the dedicated field `near_duplicates`.

If the process is still ongoing you will get an adequate status code answer ("STARTED" or "PENDING") meaning that you have to try again a bit later with another `GET` call. 

<aside class="notice">
In case of SUCCESS, results are promptly deleted afterwards, i.e. performing another GET on the same task_id will return no results.
</aside>

<aside class="success">
Remember — insert your credentials for authentication!
</aside>
