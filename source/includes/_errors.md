# Return Codes & Errors

YonderAPI returns codes that follow the HTTP standard.

## Successfull requests

When everything goes fine, YonderAPI returns HTTP codes of the type `2xx`:

Error Code | Meaning
---------- | -------
200 | OK
201 | CREATED
202 | ACCEPTED
204 | NO CONTENT

## Client-side errors

When something goes wrong on the request side, YonderAPI returns HTTP error codes of type `4xx`:

Error Code | Meaning
---------- | -------
400 | BAD REQUEST (e.g. a required parameter is missing)
401 | UNAUTHORIZED (e.g. wrong credentials)
404 | NOT FOUND (e.g. misspelled resource)
405 | METHOD NOT ALLOWED (e.g. `GET` is requested but only `POST` is available)

Error messages are self-explanatory and clearly point where the problem is. 
Examples of some possible error responses are provided aside:



```
{
    "message": {
        "language": "AR language is not supported."
    }
}
```


```
{
    "message": {
        "language": "Text and taxonomy languages do not match."
    }
}
```


```
{
    "message": {
        "text": "Text too short."
    }
}
```


```
{
    "message": {
        "text": "Missing required parameter in the post body."
    }
}
```


```
{
    "message": {
        "url": "Missing required parameter in the post body."
    }
}
```


```
{
    "message": {
        "url ": "Extracted text is empty. Invalid URL?"
    }
}
```


```
{
    "message": {
        "limit": "Value is too low: the minimum accepted is 3."
    }
}
```


```
{
    "message": {
        "ratelimit": "Limit of 1000000 requests/day reached for endpoint languagedetection."
    }
}
```


```
{
    "message": {
        "url": "Unsuccessful text extraction. Invalid URL?"
    }
}
```

```
{
  "message": {
    "collection": "The collection you are trying to create already exists."
  }
}
```


```
{
  "message": {
    "collection": "The collection you are trying to access does not exist."
  }
}
```


```
{
  "message": {
    "collection": "Error while processing your request."
  }
}
```


```
{
  "message": {
    "collection": "The document you are trying to access does not exist."
  }
}
```


```
{
  "message": {
    "collection": "The id is not a valid ObjectId."
  }
}
```



```
{
  "message": {
    "collection": "The collection name you choose is reserved."
  }
}
```



```
{
  "message": {
    "collection": "The collection you are trying to access is full (100,000 documents)."
  }
}
```

```
{
  "message": {
    "collection": "You reached the maximum allowed number of collections (1000)."
  }
}
```



## Server-side errors

When something goes wrong on the API side, YonderAPI returns HTTP error code `500 INTERNAL SERVER ERROR` with a message body such as the ones provided aside:


```
{
    "message": {
        "error": "API processing error - Code 001." 
    }
}
```




