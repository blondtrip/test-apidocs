## Taxonomy Classification 

> Request example - `POST fromURL`...


```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/text/taxonomyclassification/fromURL?limit=3&taxonomy=news-en&access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):


```json
{
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
 "topics": [
    {
      "category": "disasters and accidents",
      "score": 0.43174993460965,
      "level": 0
    },
    {
      "category": "corporate/industrial",
      "sublevels": [
        {
          "category": "regulation/policy",
          "score": 0.4917200176977,
          "level": 1
        },
        {
          "category": "capacity/facilities",
          "score": 0.34327137126374,
          "level": 1
        },
        {
          "category": "production/services",
          "score": 0.16500861103856,
          "level": 1
        }
      ],
      "score": 0.31752167325834,
      "level": 0
    },
    {
      "category": "crime, law enforcement",
      "score": 0.25072839213201,
      "level": 0
    }
  ],
  "levels": 2,
  "limit": 3,
  "taxonomy": "news-en"
}
```


> Request example - `POST fromText`...

```shell
curl --ssl-reqd --request POST --data text="The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]" "https://api.yonderlabs.com/1.0/text/taxonomyclassification/fromText?limit=3&taxonomy=news-en&access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):


```json
{
  "url": null, 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that [...]", 
  "topics": [
    {
      "category": "disasters and accidents",
      "score": 0.43174993460965,
      "level": 0
    },
    {
      "category": "corporate/industrial",
      "sublevels": [
        {
          "category": "regulation/policy",
          "score": 0.4917200176977,
          "level": 1
        },
        {
          "category": "capacity/facilities",
          "score": 0.34327137126374,
          "level": 1
        },
        {
          "category": "production/services",
          "score": 0.16500861103856,
          "level": 1
        }
      ],
      "score": 0.31752167325834,
      "level": 0
    },
    {
      "category": "crime, law enforcement",
      "score": 0.25072839213201,
      "level": 0
    }
  ],
  "levels": 2,
  "limit": 3,
  "taxonomy": "news-en"
}
```





**Categorize your text into a hierarchical taxonomy**

This service analyzes chunks of text (from single sentences to full documents) and classifies them into customizable hierarchical taxonomies (e.g. Reuters taxonomy for news, etc.). 
Allowed input sources are: text content contained in an URL ("from URL") or just simple text ("from text").


### Taxonomy Classification - `POST fromURL`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the text document | use [url-encoding](http://www.url-encode-decode.com/)|


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
taxonomy | string, required |which taxonomy to use | "news-en", "news-it", "iab-it" |
levels | number, optional | # of hierarchical levels considered for classification | 1, 2, ..., all levels (default)|
limit | number, optional | max # of relevant categories returned per each level of the taxonomy | 1, 2, 3 (default) |
access_token | string, required | your access token (40 digits) | - |


where:

+ "news-en" is the [Reuters taxonomy](http://www.ai.mit.edu/projects/jmlr/papers/volume5/lewis04a/a16-rbb-topic/topics.rbb) for news in English language;

+ "news-it" is one news taxonomy specific for Italian language;

+ "iab-it" is the [IAB (QAG) taxonomy](http://www.iab.com/guidelines/iab-quality-assurance-guidelines-qag-taxonomy/) in Italian language.

Examples of how-to-call the API and the related output are provided in the right panel.

### Taxonomy Classification - `POST fromText`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
text | string, required | the text to be classified | pass the text between "" (e.g. "This is an example") or use [url-encoded](http://www.url-encode-decode.com/) text|


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
taxonomy | string, required |which taxonomy to use | "news-en", "news-it", "iab-it" |
levels | number, optional | # of hierarchical levels considered for classification | 1, 2, ..., all levels (default)|
limit | number, optional | max # of relevant categories returned per each level of the taxonomy | 1, 2, 3 (default) |
access_token | string, required | your access token (40 digits) | - |


where:

+ "news-en" is the [Reuters taxonomy](http://www.ai.mit.edu/projects/jmlr/papers/volume5/lewis04a/a16-rbb-topic/topics.rbb) for news in English language;

+ "news-it" is one news taxonomy specific for Italian language;


+ "iab-it" is the [IAB (QAG) taxonomy](http://www.iab.com/guidelines/iab-quality-assurance-guidelines-qag-taxonomy/) in Italian language.


Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication! 
</aside>



