# Interview Questions

## System Design

- Design an API architecture for image sharing application

## Take Home Coding

- Deploy an API with a GET “hello world” route.
    - Based on client request, return JSON, or HTML.
    - Add a POST route.
    - Create a cookie for the user’s session.

# API Architectures

- REST
- GraphQL
- SOAP
- RPC

# REST

## Examples

```jsx
GET "<https://api.dictionaryapi.dev/api/v2/entries/en/chicken>"
```

## API accept data via URL parameters, or a request body.

- There is no set definition about when to use either request body or Url params, but, here are some suggestions:

|URL Params|Request Body|
|---|---|
|Non-sensitive data|Large Number of arguments|
|Key Value pair|Not Human readable|
|Length Limit|Non key : value structured data|

## API Architecture

- All APIs run on a server
    
- Microservice architecture = many APIs
    
- Design an API architecture for an image sharing application
    
- What is an API Gateway?
    
    - Kubernetes
        
        [Introduction - Kubernetes Gateway API](https://gateway-api.sigs.k8s.io/)
        
    - AWS
        
        [API Management - Amazon API Gateway - AWS](https://aws.amazon.com/api-gateway/)
        
        [What is Amazon API Gateway? - Amazon API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html)
        
        [Amazon API Gateway Get Started | API Management | Amazon Web Services](https://aws.amazon.com/api-gateway/getting-started/)
        
    - Load Balancer
        
    - Routing traffics to the correct API servers
        
    - Authentication
        
    - Security
        
    - Scaling
        
    - Metrics
        

# HTTP Basics

- What is API Gateway?
    
- Describe a framework you can use to deploy an API.
    
- URL Structure
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/3ceb816e-a14c-40cc-962a-d728b4c06672/Untitled.png)
    
- Explain the difference between `[api.site.com](<http://api.site.com>)` and `[site.com/api](<http://site.com/api>)`?
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/e9d41543-d9a6-4ba4-853c-8cfdd6a35ae8/Untitled.png)
    
- What path or method would you use for writing an endpoint for verifying a resource’s existence?
    
    `GET /users/{id}`
    
- What are the different types of HTTP methods?
    
    - Create: POST
    - Read: GET
    - Update: PUT, PATCH
    - Delete: DELETE
    - OPTIONS, HEAD, TRACE, CONNECT
    
    **Understand each HTTP method**
    
    For each method, consider the Url path: `/users/{id}`
    
    - `/users` represents a collection of users in our database
        
    - `{id}` represents an specific user id
        
    - **POST** - create new subordinate resource
        
        `POST /users`
        
        - Service creates a new `user` resource and inserts it into `users` (parent) collection
        
        Example:
        
        - User enters info and clicks “Sign Up”
        - `POST` the user info to API
        - API returns `Location` header, `/users/user123abc`
    - **GET** - read existing resource
        
        `GET /users`
        
        - returns a list of users - pagination!!
        
        `GET /users/user123abc`
        
        - returns a specific user, if it exists
        - if not, `404, not found`
        
        You can specify response type.
        
        Should NEVER modify any resources on the server
        
    - **PUT** - update an existing resource
        
        `PUT /users/{id}`
        
        - update/replace a specific resource
        
        Generally, should not be used to create a new resource
        
    - **PATCH** - update an existing resource
        
        `PATCH /users/{id}`
        
        - update a partial resource
    - **PATCH vs. PUT**
        
        - patch is non-idempotent
        - put is idempotent
        - patch can save you some bandwidth
        - put is arguably more useful, because the idempotency allows to avoid collisions and race conditions
    - **DELETE** - delete existing resource
        
        `DELETE /users`
        
        - delete collection if exists
        
        `DELETE /users/{id}`
        
        - delete specific resource if exists
        - if not, `404, not found`
        
        Common to return the deleted item in the response
        
- What types of HTTP methods are idempotent?
    
    - A request is idempotent if multiple calls with the same data result in the same outcome on the server
    - Which are idempotent?
        - `GET /users/user123abc` - idempotent
        - `POST /users` - not idempotent - applying post 10 times will create 10 new users
        - `PUT /users/{id}` - idempotent - basically, overwriting. If I add an my email to a form and press save button 10 times, the server will have my email.
        - `DELETE /users/{id}` - idempotent - no matter how many time I delete, the resource will not be there.
- Idempotency key
    
    We can make POST or PUT idempotent by adding idempotency key. Idempotency key is a unique string that identifies the request. For example, if we are using POST to create a (financial) transaction and we want to make sure, we don’t make double charges. We can add an idempotency key and include that in the request, then on the server side, we can check if there exists a record history with the same idempotency key.
    
- When would idempotent methods be used?
    
- Which request headers are commonly used? Describe uses for them
    
    [HTTP headers - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
    
- What is a cookie?
    
    - A piece of information that is saved on the client side
        - If you login to a website
            - you don’t have to login every time, whenever, you go to another page,
            - because you have authentication token stored in a cookie
- What are some uses for a cookie?
    
    session management, personalization, tracking
    
- Explain some limits you can place on your API
    
    - throttle API
    - put an authentication limit on an API and limit who can call it
- List 5 different response codes you could use in your API
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/fe1ff105-8140-481f-8b99-a4acc7d7527b/Untitled.png)
    
- What HTTP status codes are used and when?
    
    [HTTP response status codes - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
    
- Briefly explain HTTP caching. Outline a caching strategy for an image sharing application
    
- Design an API for the image sharing application with GET, POST and PUT endpoints. Outline which response codes you would use for certain situations on each endpoint
    

## Request/Response Headers

**Request headers** contain more information

- about the resource to be fetches, or
    
- about the client requesting the resource.
    
- MDN
    
    [Request header - MDN Web Docs Glossary: Definitions of Web-related terms | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Request_header)
    

**Response headers** hold additional information

- about the response, like its location or
    
- about the server providing it
    
- MDN
    
    [Response header - MDN Web Docs Glossary: Definitions of Web-related terms | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Response_header)
    

Headers often used for Authentication, Caching, Cookies, and Content Types

## Browser Cookies

A piece of data that are stored in a browser

Used for

- session management - When I log into Facebook, the server sends response with the authentication token. The authentication token is used when I tried to access the page again without logging back in. So, this information is stored in a cookie, and the cookies are automatically attached to every subsequent requests to the server.
- personalization
- tracking

## API Limits

Timeout

URL Length

Body Length

Cookie Limit

Throttling / Rate Limiting

## HTTP Caching

Shared Cache

Private Cache

- MDN
    
    [HTTP caching - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/999bc7f3-33b3-44ba-a11e-2c57d2d8c851/Untitled.png)
    
- Cache-Control
    
    `Cache-Control: private`
    
    [Cache-Control - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)
    
    ```
    cache-control max-age=0             # one week
    cache-control max-age=604800        # one month
    cache-control max-age=2592000       # one year
    cache-control no-cache              # don't cache
    cache-control no-store              # don't cache
    """
    The no-store directive prevents a response from being stored, but does not delete any already-stored response for the same URL.
    
    In other words, if there is an old response already stored for a particular URL, returning no-store will not prevent the old response from being reused.
    
    However, a no-cache directive will force the client to send a validation request before reusing any stored response.
    """
    
    cache-control public, max-age=31536000
    """
    The public directive should only be used if there is a need to store the response when the Authorization header is set. It is not required otherwise, because a response will be stored in the shared cache as long as max-age is given.
    So if the response is personalized with basic authentication, the presence of public may cause problems. 
    """
    ```
    

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/2ed61bdb-0219-4685-a42b-a9af4f30ddb7/Untitled.png)

## Response Codes

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/81f23439-1a8f-4970-aeb6-11dda6aba1ae/Untitled.png)

[HTTP response status codes - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

# REST & GraphQL

- What makes an API RESTful?
    
    **RE**presentational **S**tate **T**ransfer
    
    - required constraints
        - Uniform Interface
        - Stateless
        - Cacheable
        - Client-Server
        - Layered System
- What are the required pieces in making a GraphQL API?
    
- When should you use REST or GraphQL?
    
- What is GraphQL? What are a couple differences from REST?
    
- Explain the benefits and drawbacks of using GraphQL vs REST APIs
    
- What issues typically arise when using REST APIs?
    
- Case Study: Expose a database using an API
    
- Take Home Coding: Build a “hello word” GraphQL API
    

# Authentication

# Threats

# Testing APIs

# API Design and Implementation