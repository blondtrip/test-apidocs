## Entity Graph 

> Request example to "Create an Entity Graph" - `POST`...


```shell
curl --ssl-reqd --include --request POST "https://api.yonderlabs.com/1.0/textcollection/entitygraph?collection_name=scrooge&limit=5&access_token=YOUR_ACCESS_TOKEN"
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
  "task_type": "EntityGraphAPI", 
  "collection-name": "scrooge", 
  "task_id": "a4e31278-4432-43da-8fbf-1b21562d02f9", 
  "task_status": "PENDING"
}
```

> Request example to "Get results from Entity Graph" - `GET`...


```shell
curl --ssl-reqd --header "API-instance: instance01" --request GET "https://api.yonderlabs.com/1.0/textcollection/entitygraph?task_id=a4e31278-4432-43da-8fbf-1b21562d02f9&access_token=YOUR_ACCESS_TOKEN"
```


>... and response body, case 1) SUCCESS, i.e. the task is over:

```json
{
  "task_error": null,
  "task_type": "EntityGraphAPI",
  "task_id": "a4e31278-4432-43da-8fbf-1b21562d02f9",
  "collection_name": "scrooge",
  "task_result": {
    "timestamp": "2016-05-06 09:31:44.987771",
    "nodes": [
      {
        "count": 2,
        "info": "Malaysia (/məˈleɪʒə/ mə-LAY-zhə or /məˈleɪsiə/ mə-LAY-see-ə) (Malaysian pronunciation: [məlejsiə]) is a federal constitutional monarchy located in [...]",
        "name": "Malaysia",
        "neighbors": [
          {
            "edge_weight": 0.02197802197802198,
            "id": 1,
            "edge_count": 2
          },
          {
            "edge_weight": 0.02197802197802198,
            "id": 2,
            "edge_count": 2
          },
          {
            "edge_weight": 0.01098901098901099,
            "id": 3,
            "edge_count": 1
          },
          {
            "edge_weight": 0.01098901098901099,
            "id": 4,
            "edge_count": 1
          },
          {
            "edge_weight": 0.01098901098901099,
            "id": 5,
            "edge_count": 1
          }
        ],
        "weight": 0.012578616352201259,
        "type": "Place",
        "id": 0
      },
      {
        "count": 2,
        "info": "Kuala Lumpur is the federal capital and most populous city in Malaysia [...]",
        "name": "Kuala Lumpur",
        "neighbors": [
          {
            "edge_weight": 0.02197802197802198,
            "id": 0,
            "edge_count": 2
          },
          {
            "edge_weight": 0.02197802197802198,
            "id": 2,
            "edge_count": 2
          },
          {
            "edge_weight": 0.01098901098901099,
            "id": 3,
            "edge_count": 1
          },
          {
            "edge_weight": 0.01098901098901099,
            "id": 4,
            "edge_count": 1
          },
          {
            "edge_weight": 0.01098901098901099,
            "id": 5,
            "edge_count": 1
          }
        ],
        "weight": 0.012578616352201259,
        "type": "Place",
        "id": 1
      }
    ],
      "general_info": {
      "edge_type": "sentence",
      "number_of_nodes": 4458,
      "number_of_edges": 73867,
      "density": 0.007435287372392373
    },
    "limit": 5
  },
  "task_status": "SUCCESS"
}      
```




>... and response body, case 2) STARTED (the task has started, but it is not over):

```json
{
  "task_type": "EntityGraphAPI", 
  "task_id": "a4e31278-4432-43da-8fbf-1b21562d02f9", 
  "task_status": "STARTED"
}
```

>... and response body, case 3) PENDING (the task is still pending):

```json
{
  "task_type": "EntityGraphAPI", 
  "task_id": "a4e31278-4432-43da-8fbf-1b21562d02f9", 
  "task_status": "PENDING"
}
```


**Identify a graph of entities from your Text Collection**

This API analyzes a collection of texts and extracts a graph with most related named entities, highlighting hidden interactions between people, places and organizations.



<aside class="notice">
Depending on the size of the Text Collection, this service might take up to few seconds to provide a full answer.  
</aside>

### Create an Entity Graph - `POST`

This API allows you to launch the task which computes a co-occurrence graph on all named entities contained in a Text Collection.
Co-occurrency is here evaluated at 'sentence' level.
As detailed in the right panel, as an immediate response to this API, you will get a `202` answer ("ACCEPTED") containing a task identifier `task_id` to be used later in the `GET` call. 

Please notice that the `--include` in the `POST` call displays the response header, which includes the `API-instance` field. The value of `API-instance` field (e.g. `instance01`) must be included later in the following `GET` call.

Parameter | Type | Description | 
--------- | ------- | ----------- | 
collection_name | string, required | the name of the Text Collection from which to build an Entity Graph | 
limit	| number, optional	| max # of relevant entities to be returned, in decreasing order of edge weight (if not specified, all results are returned)
access_token | string, required | your access token (40 digits) |



### Get results from Entity Graph - `GET`

This API allows you to retrieve the computed co-occurrence graph on all named entities contained in a Text Collection, where co-occurrency is evaluated at 'sentence' level.
Please notice that the value of the `API-instance` field shown in the response header of the previous `POST` call (e.g. `instance01`) must be included in the `GET` call after the option `--header`, as detailed in the right panel.


Parameter | Type | Description | 
--------- | ------- | ----------- | 
task_id | string, required | the identifier of the created Entity Graph task| 
access_token | string, required | your access token (40 digits) |

If results are ready (i.e. the entity graph has been computed) you will get a `200` answer ("SUCCESS") and the resulting ouput, as detailed in the right panel.
If the process is still ongoing you will get an adequate status code answer ("STARTED" or "PENDING") meaning that you have to try again a bit later with another `GET` call. 

<aside class="notice">
In case of SUCCESS, results are promptly deleted afterwards, i.e. performing another GET on the same task_id will return no results.
</aside>

<aside class="success">
Remember — insert your credentials for authentication!
</aside>