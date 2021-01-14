## Text Extraction

> Request example - `POST`...



```shell
curl --ssl-reqd --request POST --data url=https%3A%2F%2Fwww.theguardian.com%2Fworld%2F2016%2Fjul%2F22%2Fmissing-flight-mh370-hunt-for-debris-will-not-be-extended "https://api.yonderlabs.com/1.0/text/textextraction?access_token=YOUR_ACCESS_TOKEN"
```

> ... and response body (200/JSON):

```json
{
  "url": "https://www.theguardian.com/world/2016/jul/22/missing-flight-mh370-hunt-for-debris-will-not-be-extended", 
  "text": "The hunt for Malaysia Airlines flight MH370 is to be suspended if evidence of the missing jet is not found in the current search area. The transport ministers of Australia, Malaysia and China, representing the country leading the search, the airline and the home of the majority of its passengers, met to discuss the future of the search in the Malaysian federal administrative centre of Putrajaya on Friday. They announced that it would \u201cnot end, but be suspended\u201d if the completion of the two-year search of a 120,000 sq km arc of the southern Indian ocean west of Australia fails to yield any new evidence. Less than 10,000 sq km of that area remain, though progress is slow due to poor weather conditions. In a joint statement, the ministers acknowledged that \u201cdespite the best efforts of all involved, the likelihood of finding the aircraft is fading. \u201cIn the absence of credible new evidence leading to an identification of a specific location of the aircraft, the search would not end, but be suspended upon completion of the 120,000 sq km area.\u201d Liow Tiong Lai, the Malaysian transport minister, told reporters that cost was not a factor in the decision. It was stressed that this did not mean the termination of the search, and that the aspiration to locate MH370 remained. But any next steps would be dependant on new information that could be used to identify the specific location of the aircraft. \u201cWe remain hopeful that the aircraft will be located,\u201d said Darren Chester, the Australian minister for transport and infrastructure. The families of the 239 victims were informed before the press conference on Friday afternoon. \u2014 Sumisha Naidu (@SumishaCNA) July 22, 2016  This does not mean we have given up on the search for #MH370   - @liowtionglai pic.twitter.com/QrAi4ewYvF That the search would not be extended in the absence of any significant discovery has been consistently signalled by the Australian body in charge for more than a year. The Australian Transport Safety Bureau has led the underwater operation for the wreckage of the missing aircraft, which disappeared en route from Kuala Lumpur to Beijing in March 2014. Chester said in a statement on Thursday that the search had been \u201cunprecedented in both size and scale, conducted in some of the world\u2019s most isolated waters and at times in extremely challenging weather\u201d. Progress on the final 10,000 or so sq km of the total search area \u2013 about the size of Greece \u2013 has been delayed by poor weather, meaning the search could extend into spring. In March, on the two-year anniversary of the plane\u2019s disappearance, Martin Dolan, the head of the ATSB, said it was \u201cvery likely\u201d the wreckage would be found within that area. But with that possibility dwindling with every square kilometre completed, experts have been forced to consider alternatives. The three countries agreed in April last year not to extend the search area beyond that 120,000 sq km. Paul Kennedy, the project director of Fugro \u2013 the Dutch company leading the search \u2013 acknowledged on Thursday that, if the plane was not found there, \u201cit means it\u2019s somewhere else\u201d. The company later clarified that it believed the search area was the most probable place and as such the right place to search. But Richard Godfrey, a member of the so-called Independent Group of professionals conducting their own work to locate MH370, argued in a paper published earlier in July that the ATSB were looking in the wrong place. He identified a range of latitudes consistent with known data, ocean drift analyses and floating debris that was not captured in the priority search area. \u201cThe failure to find sunken wreckage ... is not surprising,\u201d he wrote. \u201cThe underwater search has produced no results so far and the assumptions made in determining the ATSB priority search area should be re-examined.\u201d To date, four pieces have been identified as almost certainly being from MH370, in addition to a wing flaperon found on La R\u00e9union in July last year. A large piece of aircraft debris found on an island off the coast of Tanzania in June arrived in Canberra for examination earlier this week. It is thought to be a wing flap, but technical specialists from the ATSB are working with Malaysian investigators to determine whether it is from MH370."
}
```

**Extract text from a webpage removing all other undesired content**

This service extracts the main text from a webpage, discarding navigation links, advertisements and other undesired content.

### Text Extraction - `POST`

Attribute | Type | Description | Values |
--------- | ------- | ----------- | ------ |
url | string, required | the URL of the text document | use [url-encoding](http://www.url-encode-decode.com/)|

Parameter | Type | Description | 
--------- | ------- | ----------- | 
access_token | string, required | your access token (40 digits) |

Examples of how-to-call the API and the related output are provided in the right panel.

<aside class="success">
Remember — insert your credentials for authentication!
</aside>





