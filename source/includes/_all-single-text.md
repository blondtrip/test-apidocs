## All Single Text 

> Request example - `POST fromURL`...


```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/text/allsingletext/fromURL?access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):


```json
{
  "lang": "en", 
  "lang-ext": "English", 
  "sentiment": "neutral", 
  "tags": [
    "disasters and accidents", 
    "mh370", 
    "atsb", 
    "sumisha naidu", 
    "martin dolan", 
    "malaysia",
    "search",
    "area"
  ], 
  "reactions": [
    {
      "reaction": "wow", 
      "score": 0.51
    }, 
    {
      "reaction": "sad", 
      "score": 0.49
    }
  ], 
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "topics": [
    {
      "category": "disasters and accidents", 
      "score": 0.43648842879859323, 
      "level": 0
    }, 
    {
      "category": "corporate/industrial", 
      "sublevels": [
        {
          "category": "regulation/policy", 
          "score": 0.48749040688621503, 
          "level": 1
        }, 
        {
          "category": "capacity/facilities", 
          "score": 0.3472713949921758, 
          "level": 1
        }, 
        {
          "category": "production/services", 
          "score": 0.1652381981216092, 
          "level": 1
        }
      ], 
      "score": 0.29542684300638344, 
      "level": 0
    }, 
    {
      "category": "crime, law enforcement", 
      "score": 0.2680847281950233, 
      "level": 0
    }
  ], 
    "summary": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. “In the absence of credible new evidence leading to an identification of a specific location of the aircraft, the search would not end, but be suspended upon completion of the 120,000 sq km area.” Liow Tiong Lai, the Malaysian transport minister, told reporters that cost was not a factor in the decision. “The underwater search has produced no results so far and the assumptions made in determining the ATSB priority search area should be re-examined.” To date, four pieces have been identified as almost certainly being from MH370, in addition to a wing flaperon found on La Réunion in July last year. It is thought to be a wing flap, but technical specialists from the ATSB are working with Malaysian investigators to determine whether it is from MH370.",
  "entities": [
    {
      "info": null, 
      "score": 1.0, 
      "type": "Organization", 
      "name": "MH370"
    }, 
    {
      "info": null, 
      "score": 1.0, 
      "type": "Organization", 
      "name": "ATSB"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Malaysia", 
        "description": "Malaysia (/m\u0259\u02c8le\u026a\u0292\u0259/ m\u0259-LAY-zh\u0259 or /m\u0259\u02c8le\u026asi\u0259/ m\u0259-LAY-see-\u0259) (Malaysian pronunciation: [m\u0259lejsi\u0259]) is a federal constitutional monarchy [...]"
      }, 
      "score": 0.6, 
      "type": "Place", 
      "name": "Malaysia"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Australia", 
        "description": "Australia /\u0252\u02c8stre\u026ali\u0259/, /\u0259-/, or colloquially /-j\u0259/, officially the Commonwealth of Australia, is an Oceanian country [...]"
      }, 
      "score": 0.6, 
      "type": "Place", 
      "name": "Australia"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Chester", 
        "description": "Chester (/\u02c8t\u0283\u025bst\u0259r/ CHESS-t\u0259r), is a city in Cheshire, England. Lying on [...]"
      }, 
      "score": 0.6, 
      "type": "Place", 
      "name": "Chester"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/China", 
        "description": "China (/\u02c8t\u0283a\u026an\u0259/; simplified Chinese: \u4e2d\u56fd; traditional Chinese: \u4e2d\u570b; pinyin: Zh\u014dnggu\u00f3), officially the People's Republic of China (PRC), is a sovereign state [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "China"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Sumisha_Naidu", 
        "description": "Sumisha Naidu is a former Australian Broadcasting Corporation and KiniTV journalist and presenter [...]"
      }, 
      "score": 0.2, 
      "type": "Person", 
      "name": "Sumisha Naidu"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Kuala_Lumpur", 
        "description": "Kuala Lumpur (/\u02c8kw\u0251\u02d0l\u0259\u02c8l\u028amp\u028a\u0259r/ or /-p\u0259r/; Malaysian pronunciation: [\u02c8kwal\u0259 \u02c8lump\u028ar]), is the federal capital and [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Kuala Lumpur"
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
        "wikipedia": "http://en.wikipedia.org/wiki/Tanzania", 
        "description": "Tanzania /\u02cct\u00e6nz\u0259\u02c8ni\u02d0\u0259/, officially the United Republic of Tanzania (Swahili: Jamhuri ya Muungano wa Tanzania), is a country in East Africa [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Tanzania"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Putrajaya", 
        "description": "Putrajaya is a planned city, 25 km south of Kuala Lumpur [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Putrajaya"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Greece", 
        "description": "Greece  (Greek: \u0395\u03bb\u03bb\u03ac\u03b4\u03b1, Ell\u00e1da, pronounced [e\u02c8la\u00f0a] (13px )), officially the Hellenic Republic (\u0395\u03bb\u03bb\u03b7\u03bd\u03b9\u03ba\u03ae \u0394\u03b7\u03bc\u03bf\u03ba\u03c1\u03b1\u03c4\u03af\u03b1 [elini\u02c8ci \u00f0imokra\u02c8ti.a] Ell\u012bnik\u012b\u0301 D\u012bmokrat\u00eda) and known since ancient times as Hellas [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Greece"
    }
  ], 
  "keywords": [
    {
      "score": 1.0, 
      "name": "search"
    }, 
    {
      "score": 1.0, 
      "name": "area"
    }, 
    {
      "score": 1.0, 
      "name": "sq km"
    }, 
    {
      "score": 1.0, 
      "name": "aircraft"
    }, 
    {
      "score": 0.9, 
      "name": "ministers"
    }, 
    {
      "score": 0.9, 
      "name": "completion"
    }, 
    {
      "score": 0.9, 
      "name": "remain"
    }, 
    {
      "score": 0.4, 
      "name": "transport"
    }, 
    {
      "score": 0.4, 
      "name": "country"
    }, 
    {
      "score": 0.4, 
      "name": "end"
    }, 
    {
      "score": 0.4, 
      "name": "poor weather"
    }, 
    {
      "score": 0.4, 
      "name": "absence"
    }, 
    {
      "score": 0.4, 
      "name": "specific location"
    }, 
    {
      "score": 0.4, 
      "name": "wreckage"
    }, 
    {
      "score": 0.4, 
      "name": "plane"
    }
  ]
}
```


> Request example - `POST fromText`...

```shell
curl --ssl-reqd --request POST --data text="The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]" "https://api.yonderlabs.com/1.0/text/allsingletext/fromText?access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):


```json
{
  "lang": "en", 
  "lang-ext": "English", 
  "sentiment": "neutral", 
  "tags": [
     "disasters and accidents", 
    "mh370", 
    "atsb", 
    "sumisha naidu", 
    "martin dolan", 
    "malaysia",
    "search",
    "area"
  ], 
  "reactions": [
    {
      "reaction": "wow", 
      "score": 0.51
    }, 
    {
      "reaction": "sad", 
      "score": 0.49
    }
  ], 
  "url": null, 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "topics": [
    {
      "category": "disasters and accidents", 
      "score": 0.43648842879859323, 
      "level": 0
    }, 
    {
      "category": "corporate/industrial", 
      "sublevels": [
        {
          "category": "regulation/policy", 
          "score": 0.48749040688621503, 
          "level": 1
        }, 
        {
          "category": "capacity/facilities", 
          "score": 0.3472713949921758, 
          "level": 1
        }, 
        {
          "category": "production/services", 
          "score": 0.1652381981216092, 
          "level": 1
        }
      ], 
      "score": 0.29542684300638344, 
      "level": 0
    }, 
    {
      "category": "crime, law enforcement", 
      "score": 0.2680847281950233, 
      "level": 0
    }
  ], 
    "summary": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. “In the absence of credible new evidence leading to an identification of a specific location of the aircraft, the search would not end, but be suspended upon completion of the 120,000 sq km area.” Liow Tiong Lai, the Malaysian transport minister, told reporters that cost was not a factor in the decision. “The underwater search has produced no results so far and the assumptions made in determining the ATSB priority search area should be re-examined.” To date, four pieces have been identified as almost certainly being from MH370, in addition to a wing flaperon found on La Réunion in July last year. It is thought to be a wing flap, but technical specialists from the ATSB are working with Malaysian investigators to determine whether it is from MH370.",
  "entities": [
    {
      "info": null, 
      "score": 1.0, 
      "type": "Organization", 
      "name": "MH370"
    }, 
    {
      "info": null, 
      "score": 1.0, 
      "type": "Organization", 
      "name": "ATSB"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Malaysia", 
        "description": "Malaysia (/m\u0259\u02c8le\u026a\u0292\u0259/ m\u0259-LAY-zh\u0259 or /m\u0259\u02c8le\u026asi\u0259/ m\u0259-LAY-see-\u0259) (Malaysian pronunciation: [m\u0259lejsi\u0259]) is a federal constitutional monarchy [...]"
      }, 
      "score": 0.6, 
      "type": "Place", 
      "name": "Malaysia"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Australia", 
        "description": "Australia /\u0252\u02c8stre\u026ali\u0259/, /\u0259-/, or colloquially /-j\u0259/, officially the Commonwealth of Australia, is an Oceanian country [...]"
      }, 
      "score": 0.6, 
      "type": "Place", 
      "name": "Australia"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Chester", 
        "description": "Chester (/\u02c8t\u0283\u025bst\u0259r/ CHESS-t\u0259r), is a city in Cheshire, England. Lying on [...]"
      }, 
      "score": 0.6, 
      "type": "Place", 
      "name": "Chester"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/China", 
        "description": "China (/\u02c8t\u0283a\u026an\u0259/; simplified Chinese: \u4e2d\u56fd; traditional Chinese: \u4e2d\u570b; pinyin: Zh\u014dnggu\u00f3), officially the People's Republic of China (PRC), is a sovereign state [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "China"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Sumisha_Naidu", 
        "description": "Sumisha Naidu is a former Australian Broadcasting Corporation and KiniTV journalist and presenter [...]"
      }, 
      "score": 0.2, 
      "type": "Person", 
      "name": "Sumisha Naidu"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Kuala_Lumpur", 
        "description": "Kuala Lumpur (/\u02c8kw\u0251\u02d0l\u0259\u02c8l\u028amp\u028a\u0259r/ or /-p\u0259r/; Malaysian pronunciation: [\u02c8kwal\u0259 \u02c8lump\u028ar]), is the federal capital and [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Kuala Lumpur"
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
        "wikipedia": "http://en.wikipedia.org/wiki/Tanzania", 
        "description": "Tanzania /\u02cct\u00e6nz\u0259\u02c8ni\u02d0\u0259/, officially the United Republic of Tanzania (Swahili: Jamhuri ya Muungano wa Tanzania), is a country in East Africa [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Tanzania"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Putrajaya", 
        "description": "Putrajaya is a planned city, 25 km south of Kuala Lumpur [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Putrajaya"
    }, 
    {
      "info": {
        "wikipedia": "http://en.wikipedia.org/wiki/Greece", 
        "description": "Greece  (Greek: \u0395\u03bb\u03bb\u03ac\u03b4\u03b1, Ell\u00e1da, pronounced [e\u02c8la\u00f0a] (13px )), officially the Hellenic Republic (\u0395\u03bb\u03bb\u03b7\u03bd\u03b9\u03ba\u03ae \u0394\u03b7\u03bc\u03bf\u03ba\u03c1\u03b1\u03c4\u03af\u03b1 [elini\u02c8ci \u00f0imokra\u02c8ti.a] Ell\u012bnik\u012b\u0301 D\u012bmokrat\u00eda) and known since ancient times as Hellas [...]"
      }, 
      "score": 0.2, 
      "type": "Place", 
      "name": "Greece"
    }
  ], 
  "keywords": [
    {
      "score": 1.0, 
      "name": "search"
    }, 
    {
      "score": 1.0, 
      "name": "area"
    }, 
    {
      "score": 1.0, 
      "name": "sq km"
    }, 
    {
      "score": 1.0, 
      "name": "aircraft"
    }, 
    {
      "score": 0.9, 
      "name": "ministers"
    }, 
    {
      "score": 0.9, 
      "name": "completion"
    }, 
    {
      "score": 0.9, 
      "name": "remain"
    }, 
    {
      "score": 0.4, 
      "name": "transport"
    }, 
    {
      "score": 0.4, 
      "name": "country"
    }, 
    {
      "score": 0.4, 
      "name": "end"
    }, 
    {
      "score": 0.4, 
      "name": "poor weather"
    }, 
    {
      "score": 0.4, 
      "name": "absence"
    }, 
    {
      "score": 0.4, 
      "name": "specific location"
    }, 
    {
      "score": 0.4, 
      "name": "wreckage"
    }, 
    {
      "score": 0.4, 
      "name": "plane"
    }
  ]
}
```


**Analyze your document with all single API on text**

This service analyzes your text content by applying at once all single API on text documents, that are:

+ Text Extraction (fromURL only)
+ Language Detection
+ Taxonomy Classification
+ Sentiment Analysis
+ Emotional Reaction
+ Entity Extraction
+ Keyword Extraction
+ Concept Tagging
+ Text Summarization


Employed taxonomies, depending on the text language, are:

+ "news-en" is the [Reuters taxonomy](http://www.ai.mit.edu/projects/jmlr/papers/volume5/lewis04a/a16-rbb-topic/topics.rbb) for news in English language;
+ "news-it" is one news taxonomy specific for Italian language.

The parameter values are the default ones of the single API (i.e. 'all' results for Entity Extraction API and Keyword Extraction API, '10' results for Concept Tagging API).
As for Entity Extraction and Concept Tagging APIs, it is possible to include custom whitelists and blacklists of entities and concepts upon request. 
Allowed input sources are: text content contained in an URL ("from URL") or just simple text ("from text").


### All Single Text - `POST fromURL`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the text document | use [url-encoding](http://www.url-encode-decode.com/)|


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
taxonomy | string, required |which taxonomy to use | "news-en", "news-it", "iab-it" |
levels_taxonomy | number, optional | # of hierarchical levels considered for classification | 1, 2, ..., all levels (default)|
limit_taxonomy | number, optional | max # of relevant categories returned per each level of the taxonomy | 1, 2, 3 (default) |
limit_entity | number, optional | max # of relevant entities to be returned, in decreasing order of confidence (if not specified, all results are returned)
limit_keyword | number, optional | max # of relevant keywords to be returned, in decreasing order of relevance (if not specified, all results are returned)
limit_concept | number, optional | max # of relevant tags to be returned, in decreasing order of relevance | 1, 2, ..., 10 (default), etc. |
nwords | number, optional | approximate number of words in the summary |   1,2, ..., 150 (default), ...
ratio | number, optional | compression ratio of the summary | [0.1, 0.2, ..., 0.9]. If 'ratio' is specified, 'nwords' is ignored

access_token | string, required | your access token (40 digits) | - |
Examples of how-to-call the API and the related output are provided in the right panel.

### All Single Text - `POST fromText`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
text | string, required | the text to be classified | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
taxonomy | string, required |which taxonomy to use | "news-en", "news-it", "iab-it" |
levels_taxonomy | number, optional | # of hierarchical levels considered for classification | 1, 2, ..., all levels (default)|
limit_taxonomy | number, optional | max # of relevant categories returned per each level of the taxonomy | 1, 2, 3 (default) |
limit_entity | number, optional | max # of relevant entities to be returned, in decreasing order of confidence (if not specified, all results are returned)
limit_keyword | number, optional | max # of relevant keywords to be returned, in decreasing order of relevance (if not specified, all results are returned)
limit_concept | number, optional | max # of relevant tags to be returned, in decreasing order of relevance | 1, 2, ..., 10 (default), etc. |
nwords | number, optional | approximate number of words in the summary |   1,2, ..., 150 (default), ...
ratio | number, optional | compression ratio of the summary | [0.1, 0.2, ..., 0.9]. If 'ratio' is specified, 'nwords' is ignored

access_token | string, required | your access token (40 digits) | - |
Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication! 
</aside>



