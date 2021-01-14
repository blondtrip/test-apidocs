## Entity Extraction


> Request example - `POST fromURL`...

```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/text/entityextraction/fromURL?limit=10&access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):

```json
{
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "limit": 10, 
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
        "description": "Chester (/ˈtʃɛstər/ CHESS-tər), is a city in Cheshire, England [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Chester"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Australia",
        "description": "Australia /ɒˈstreɪliə/, /ə-/, or colloquially /-jə/, officially the Commonwealth of Australia, is an Oceanian country [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Australia"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Malaysia",
        "description": "Malaysia (/məˈleɪʒə/ mə-LAY-zhə or /məˈleɪsiə/ mə-LAY-see-ə) (Malaysian pronunciation: [məlejsiə]) is a federal constitutional monarchy located in [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Malaysia"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Kuala_Lumpur",
        "description": "Kuala Lumpur (/ˈkwɑːləˈlʊmpʊər/ or /-pər/; Malaysian pronunciation: [ˈkwalə ˈlumpʊr]), is the federal capital and most populous city in Malaysia [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Kuala Lumpur"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/China",
        "description": "China (/ˈtʃaɪnə/; simplified Chinese: 中国; traditional Chinese: 中國; pinyin: Zhōngguó), officially the People's Republic of China (PRC), is a sovereign state [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "China"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Tanzania",
        "description": "Tanzania /ˌtænzəˈniːə/, officially the United Republic of Tanzania (Swahili: Jamhuri ya Muungano wa Tanzania), is a country in East Africa [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Tanzania"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Beijing",
        "description": "Beijing, sometimes romanized as Peking, is the capital of the People's Republic of China and [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Beijing"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Greece",
        "description": "Greece  (Greek: Ελλάδα, Elláda, pronounced [eˈlaða]), officially the Hellenic Republic (Ελληνική Δημοκρατία [eliniˈci ðimokraˈti.a] Ellīnikī́ Dīmokratía) and known since ancient times as Hellas [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Greece"
    }
  ]
}
```


> Request example - `POST fromText`...



```shell
curl --ssl-reqd --request POST --data text="The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]." "https://api.yonderlabs.com/1.0/text/entityextraction/fromText?limit=10&access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):

```json
{
  "url": null, 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...].", 
  "limit": 10, 
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
        "description": "Chester (/ˈtʃɛstər/ CHESS-tər), is a city in Cheshire, England [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Chester"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Australia",
        "description": "Australia /ɒˈstreɪliə/, /ə-/, or colloquially /-jə/, officially the Commonwealth of Australia, is an Oceanian country [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Australia"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Malaysia",
        "description": "Malaysia (/məˈleɪʒə/ mə-LAY-zhə or /məˈleɪsiə/ mə-LAY-see-ə) (Malaysian pronunciation: [məlejsiə]) is a federal constitutional monarchy located in [...]"
      },
      "score": 0.6,
      "type": "Place",
      "name": "Malaysia"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Kuala_Lumpur",
        "description": "Kuala Lumpur (/ˈkwɑːləˈlʊmpʊər/ or /-pər/; Malaysian pronunciation: [ˈkwalə ˈlumpʊr]), is the federal capital and most populous city in Malaysia [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Kuala Lumpur"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/China",
        "description": "China (/ˈtʃaɪnə/; simplified Chinese: 中国; traditional Chinese: 中國; pinyin: Zhōngguó), officially the People's Republic of China (PRC), is a sovereign state [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "China"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Tanzania",
        "description": "Tanzania /ˌtænzəˈniːə/, officially the United Republic of Tanzania (Swahili: Jamhuri ya Muungano wa Tanzania), is a country in East Africa [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Tanzania"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Beijing",
        "description": "Beijing, sometimes romanized as Peking, is the capital of the People's Republic of China and [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Beijing"
    },
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Greece",
        "description": "Greece  (Greek: Ελλάδα, Elláda, pronounced [eˈlaða]), officially the Hellenic Republic (Ελληνική Δημοκρατία [eliniˈci ðimokraˈti.a] Ellīnikī́ Dīmokratía) and known since ancient times as Hellas [...]"
      },
      "score": 0.2,
      "type": "Place",
      "name": "Greece"
    }
  ]
}
```






**Identify people, places, and organizations in your text**

This API detects named entities and classify them as `Person`, `Place`, `Organization` or `Misc`. The service also links them to knowledge base repositories (Wikipedia, DBpedia, etc.).
It is also possible to include custom whitelists and blacklists of entities upon request.
Allowed input sources are: text content contained in an URL ("from URL") or just simple text ("from text").


### Entity Extraction - `POST fromURL` 


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the text document | use [url-encoding](http://www.url-encode-decode.com/)|


Parameter | Type | Description |
--------- | ------- | ----------- | 
limit | number, optional | max # of relevant entities to be returned, in decreasing order of confidence (if not specified, all results are returned)
access_token | string, required | your access token (40 digits) | 

Examples of how-to-call the API and the related output are provided in the right panel.

### Entity Extraction - `POST fromText` 

Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
text | string, required | the text to be classified | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|



Parameter | Type | Description | 
--------- | ------- | ----------- | 
limit | number, optional | max # of relevant entities to be returned, in decreasing order of confidence (if not specified, all results are returned)
access_token | string, required | your access token (40 digits) | 

Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication!
</aside>

