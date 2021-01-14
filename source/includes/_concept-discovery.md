## Concept Discovery 

> This is the code "from url"...

```python

from urllib2 import Request, urlopen

request = Request('https://api.yonderlabs.com/1.0/text/taxonomyclassification/fromURL?url=url&taxonomy=taxonomy&levels=2&limit=3')

response_body = urlopen(request).read()
print response_body
```
```shell
curl --include \
     --request POST \
'https://api.yonderlabs.com/1.0/text/taxonomyclassification/fromURL?url=url&taxonomy=taxonomy&levels=2&limit=3'
```



>... which returs a json structured like this (response 200):

```json
{
    "text": "A wonderful tennis match took place yesterday at Wimbledon between Djokovic and Federer"
    "taxonomy": "iab"
    "levels": 2
    "limit": 3
    "topic":
        [
            {
                "level": 0
                "category": "sports"
                "score": 0.8
                "sublevels":
                    [
                        {
                            "level": 1
                            "category": "tennis"
                            "score": 1.0
                        }
                    ]
            },
            {
                "level": 0
                "category": "arts&entertainment"
                "score": 0.2
                "sublevels":
                    [
                        {
                            "level": 1
                            "category": "television"
                            "score": 0.9
                        },
                        {
                            "level": 1
                            "category": "celebrity fun/gossip"
                            "score": 0.1
                        }
                    ]
            },
        ]
}
```



> This is the code "from text"...

```python

from urllib2 import Request, urlopen

request = Request('https://api.yonderlabs.com/1.0/text/taxonomyclassification/fromText?text=text&taxonomy=taxonomy&levels=2&limit=3')

response_body = urlopen(request).read()
print response_body
```


```shell
curl --include \
     --request POST \
'https://api.yonderlabs.com/1.0/text/taxonomyclassification/fromText?text=text&taxonomy=taxonomy&levels=2&limit=3'
```

>... which returs a json structured like this (response 200):

```json
{
  "levels": 2,
  "limit": 1,
  "taxonomy": "iab-it",
  "text": "Contemporaneamente a Juncker, anche la Cancelliera Merkel parla di emergenza immigrazione, in un discorso al Bundestag. E lo fa, al solito, con i suoi toni pragmatici: « Coloro che cercano asilo e che vedono riconosciuto il diritto d’asilo hanno bisogno del nostro aiuto. E bisogna integrarli velocemente. E altrettanto velocemente devono imparare velocemente il tedesco e avere velocemente un lavoro. Diventeranno cittadini tedeschi», ha aggiunto. «Un Paese che dice “benvenuti” a tante persone deve anche dire quali sono le regole - ha aggiunto -. Anche questo fa parte di una società aperta. Non ci sarà nessuna tolleranza per la società parallela». Temi e concetti che si ritrovano anche nel discorso di Juncker.",
  "topics": [
    {
      "category": "leggi_governo_e_politica",
      "level": 0,
      "score": 0.7233245447210793,
      "sublevels": [
        {
          "category": "politica",
          "level": 1,
          "score": 0.5251832068430112
        }
      ]
    }
  ]
}
```





**Find other relevant concepts not in your text from a Text Collection**

Based on the submitted text, this API proposes contextually relevant semantic tags originally not in your text, by retrieving them from a Text Collection.

<aside class="notice">
Depending on the size of the Text Collection, this service might take up to several minutes to provide a full answer. As better detailed in the sidebar, you will get an immediate first answer containing a "ticketID" (and a "timetogo" estimation) to be used for calling again the service later on an get the full result. 
</aside>

### From URL: HTTPS Request 

`POST https://api.yonderlabs.com/1.0/textcollections/collection/conceptdiscovery/fromURL?url=url&limit=None`

Parameter | Type | Description | Values |
--------- | ------- | ----------- | ----------- |
collection | string, optional | the name of the Text Collection | "yonder" (default)
url | string, required | the URL of the text document | --- |
limit | number, optional | the max # of relevant results to be returned | If not specified, all results are returned


### From text: HTTPS Request 

`POST https://api.yonderlabs.com/1.0/textcollections/collection/conceptdiscovery/fromText?text=text&limit=None`

Parameter | Type | Description | Values |
--------- | ------- | ----------- | ----------- |
collection | string, optional | the name of the Text Collection | "yonder" (default)
text | string, required | the text document | --- |
limit | number, optional | the max # of relevant results to be returned | If not specified, all results are returned


<aside class="success">
Remember — insert your credentials for authentication!
</aside>
