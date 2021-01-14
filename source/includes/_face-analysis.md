## Face Analysis 

> Request example - `POST fromURL`...


```shell
curl --ssl-reqd --request POST --data url="http://media.salon.com/2016/01/donald_trump69.jpg" "https://api.yonderlabs.com/1.0/image/faceanalysis/fromURL?access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):


```json
{
  "url": "http://media.salon.com/2016/01/donald_trump69.jpg", 
  "image": null, 
  "image_width": 620, 
  "image_height": 412, 
  "faces": [
    {
      "position": {
        "bottom_right_y": 198, 
        "top_left_x": 288, 
        "top_left_y": 30, 
        "bottom_right_x": 455
      }, 
      "attributes": {
        "gender": "Male", 
        "age": "60-100"
      }
    }
  ], 
  "total_faces": 1
}
```


> Request example - `POST fromFile`...

```shell
curl --ssl-reqd --request POST --form image="@donald-trump.jpg" "https://api.yonderlabs.com/1.0/image/faceanalysis/fromImage?access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):


```json
{
  "url": null, 
  "image": "@donald-trump.jpg", 
  "image_width": 620, 
  "image_height": 412, 
  "faces": [
    {
      "position": {
        "bottom_right_y": 198, 
        "top_left_x": 288, 
        "top_left_y": 30, 
        "bottom_right_x": 455
      }, 
      "attributes": {
        "gender": "Male", 
        "age": "60-100"
      }
    }
  ], 
  "total_faces": 1
}
```


**Analyze faces in an image**

This service provides facial analysis on images, including detection, gender and age prediction. 
Allowed input sources are: images retrieved from an URL ("from URL") or images uploaded from files ("from file").



### Face Analysis - `POST fromURL`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the image | use [url-encoding](http://www.url-encode-decode.com/)|


Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
gender | string, optional |gender prediction | "false", "true" (default)|
age | string, optional |age prediction (beta) | "false", "true" (default)|
access_token | string, required | your access token (40 digits) | - |


Examples of how-to-call the API and the related output are provided in the right panel.

### Face Analysis - `POST fromFile`


Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
file | string, required | the path of the local image file | pass the path between "" (e.g. "@/usr/myself/Desktop/donald-trump.jpg") 



Parameter | Type | Description | Values |
--------- | ------- | ----------- | ------ |
gender | string, optional |gender prediction | "false", "true" (default)|
age | string, optional |age prediction (beta) | "false", "true" (default)|
access_token | string, required | your access token (40 digits) | - |


Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication! 
</aside>



