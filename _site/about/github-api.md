### Reading APIs (Application Programming Interface)

- An API is a set of routines, protocols and tools for building software appliactions. 

**How does the API handle authentication?**
  - Requests that require authentication will return: `404 Not Found`, instead of `403 Forbidden`, in some places. *This is to prevent the accidental leakege of private repos to unauthorized users.* 

**What can I do with an unauthenticated request?**
- Authenticating with invalid credentials will return `401 Unauthorized`
- After detecting several requests with invalid credentials within a short period, the API will temporarily reject all authentication attempts for that user (including ones with valid credentials) with `403 Forbidden`.

**How can I authenticate my request? (3 ways)**
- There are three ways to authenticate through Github API:
 - *Basic Authentication*
 - *OAuth2 Token (sent in a header)*
 - *OAuth2 Token (sent as a parameter)*

#### How do I ask the API for...

**The profile information for a specific user?**
 - 
**The repository listing for a specific user?**
- 
**The recent, public activity for a specific user?**
- 
**Is there a limit to the number of requests I can make?**
- For requests using Basic Authentication or OAuth, you can make up to 5,000 requests per hour. For unauthenticated requests, the rate limit allows you to make up to 60 requests per hour. Unauthenticated requests are associated with your IP address, and not the user making requests. 
**Is there a way of extending that limit?**
- If your OAuth application needs to make unauthenticated calls with a higher rate limit, you can pass your app’s client ID and secret as part of the query string.
```
$ curl -i 'https://api.github.com/users/whatever?client_id=xxxx&client_secret=yyyy'

HTTP/1.1 200 OK
Date: Mon, 01 Jul 2013 17:27:06 GMT
Status: 200 OK
X-RateLimit-Limit: 5000
X-RateLimit-Remaining: 4966
X-RateLimit-Reset: 1372700873
```
- This method should only be used for server-to-server calls. You should never share your client secret with anyone or include it in client-side browser code.

**What happens when I hit the limit?**
- Once you go over the rate limit you will receive an error response:
```
HTTP/1.1 403 Forbidden
Date: Tue, 20 Aug 2013 14:50:41 GMT
Status: 403 Forbidden
X-RateLimit-Limit: 60
X-RateLimit-Remaining: 0
X-RateLimit-Reset: 1377013266

{
    "message": "API rate limit exceeded for xxx.xxx.xxx.xxx. (But here's the good news: Authenticated requests get a higher rate limit. Check out the documentation for more details.)",
    "documentation_url": "https://developer.github.com/v3/#rate-limiting"
}
```
**What if there is a lot of data returned?**
- Requests that return multiple items will be paginated to 30 items by default. You can specify further pages with the `?page` parameter. 
- For some resources, you can also set a custom page size up to 100 with the ?per_page parameter. 

**How can I ask for more (or less) data from a request?**
- 
**How do I know that there is more data available?**
- 
