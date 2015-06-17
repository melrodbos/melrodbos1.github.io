**Reading APIs: Etsy**
  * [ ] How do I make API requests?
    * [ ] What is the base URL?
https://openapi.etsy.com/v2
    * [ ] Are there any headers or query parameters required? 
api key-based parameter
    * [ ] What kind of response should I expect?
Each API response is wrapped in a standard structure that holds the results of the API call, plus metadata about the request:
```
{
     "count":integer,
     "results": [
         { result object }
     ],
     "params": { parameters },
     "type":result type
}
```

count specifies the total number of results available for this call, which may be more than the number of results returned in this request. For example, if count is 1000, you can page through the results in blocks of 100 by specifying limit=100&offset=0, where offset is a multiple of 100 up to 900. See Pagination below.

results is an array of results. For consistency's sake, it is always an array, even if only one result is expected.

params echoes the parameters that were passed in the request.

type specifies the type of the objects in the results array. (See the individual pages under "API Reference".)

  * [ ] How does the API handle authentication?
The Etsy API requires an application key that is provided during app registration. The key identifies your application to the Etsy web service, and is used to track overall call usage. It's passed using the standard api_key parameter.
    * [ ] Do I need to authenticate?
Yes. 
    * [ ] What can I do with an unauthenticated request?

    * [ ] How can I authenticate my request?
The Etsy API requires an application key that is provided during app registration. The key identifies your application to the Etsy web service, and is used to track overall call usage. It's passed using the standard api_key parameter.  * [ ] How do I ask the API for...
    * [ ] A list of products belonging to a specific category or collection?
https://openapi.etsy.com/v2/listings/:listing_id
    * [ ] Details about a specific product? What details are provided?
 

    * [ ] The main and additional images for a product?
 Image uploads can be performed using a POST request with the Content-Type: multipart/form-dataheader, following RFC1867. This is identical to using curl -F, except that that request needs to be signed using OAuth.   

  * [ ] Is there a limit to the number of requests I can make?
Using public (api key-based) authentication, clients are allowed 10,000 requests per 24-hour period, with a limit of 10 queries per second.
    * [ ] Is there a way of extending that limit?
If your application needs more than the allotted number of calls, contact us at developer@etsy.com with a description of the application and an estimate on needed call usage. You might also want to investigate the use of caching to keep the number of calls to a minimum, and make your application more responsive.
    * [ ] What happens when I hit the limit?
if you hit a rate limit, you'll only need to wait for at most two more hours in order to get a few more allowed requests (the exact amount will depend on the number of requests you made in the two-hour block of 24 hours prior). 
  * [ ] What if there is a _lot_ of data returned?

    * [ ] How can I ask for more (or less) data from a request?

    * [ ] How do I know that there is more data available?
    
 What Resource in the API represents...
* an individual product?
A listing in the field location
```/v2/listings/active?fields=listings_id
```
* a group or collection of products
Shops or sections, categories

images associated with a product?
getImage_listing in the URL
```/listings/:listing_id/images/:listing_image_id
```

sizes and colors for a product?
it is represented by variations. Ex
```/v2/listings/:listing_id/variations

What would be returned

variations=[
    {"property_id":200, "value":"Black", "is_available":true, "price": 100},
    {"property_id":200, "value":"White", "is_available":true, "price": 110}
]

```

What actions and endpoints exist for each of these Resources?

What parameters do each endpoint require or accept?
What fields are returned for each Resource, specifically:
an individual product?
a group or collection of products?
What additional fields can be requested for each?
What is a Taxonomy Resource?
