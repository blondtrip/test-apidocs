## Concept Graph 

> This is the code to "Extract a graph of concepts"...

```python

from urllib2 import Request, urlopen

values = """
url=http://www.gazzetta.it/Formula-1/20-09-2015/singapore-vettel-ferrari-f1-130196268810.shtml"""

request = Request('https://api.yonderlabs.com/1.0/text/sentimentanalysis/fromURL', data=values)

response_body = urlopen(request).read()
print response_body
```

```shell
curl --include \
     --request POST \
   --data-binary "url=http://www.gazzetta.it/Formula-1/20-09-2015/singapore-vettel-ferrari-f1-130196268810.shtml" \
'https://api.yonderlabs.com/1.0/text/sentimentanalysis/fromURL'
```



>... which returs a json structured like this (response 200):

```json
{
  "sentiment": "positive",
  "url": "http://www.gazzetta.it/Formula-1/20-09-2015/singapore-vettel-ferrari-f1-130196268810.shtml"
}
```




**Identify a graph of concepts from your Text Collection**

This API analyzes a collection of texts and extract graph of interactions between entities and keywords, revealing important facts, events, and hidden relations.

<aside class="notice">
Depending on the size of the Text Collection, this service might take up to several minutes to provide a full answer. As better detailed in the sidebar, you will get an immediate first answer containing a "ticketID" (and a "timetogo" estimation) to be used for calling again the service later on an get the full result. 
</aside>

### Extract a graph of concepts 

`POST https://api.yonderlabs.com/1.0/textcollections/collection/conceptgraph?limit=None`

Parameter | Type | Description | Values |
--------- | ------- | ----------- | ----------- |
collection | string, optional | the name of the Text Collection | "yonder" (default)
limit | number, optional | the max # of relevant results to be returned | If not specified, all results are returned


Attribute | Type | Description | Values
--------- | ------- | ----------- | ----------- |
rangeids | array of number intervals, optional | the interval of Item IDs to be used | Example: rangeids = (90,100), (150,180) means consider all Items whose ID is in the interval (90,100) AND all items whose ID is in (150,180). If not specified the entire Text Collection is used



<aside class="success">
Remember — insert your credentials for authentication!
</aside>
