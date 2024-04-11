# 0. Introduction

A) **Model data** for these scenarios:

- A buy/sell marketplace (OfferUp)
- An app for streaming music and creating playlists (like Spotify)
- A homework platform

B) For each of the scenarios above, write a list of **endpoints** for a REST API

C) For each of these user **error status codes**, list two examples from the scenarios above that should return those errors:

- 400 - Bad Request (e.g., malformed request syntax, invalid request message framing, or deceptive request routing)
    
- 401 - Unauthorized (Although the HTTP standard specifies "unauthorized", semantically this response means "unauthenticated". That is, the client must authenticate itself to get the requested response)
    
- 403 - Forbidden (The client does not have access rights to the content; that is, it is unauthorized, so the server is refusing to give the requested resource. Unlike `401 Unauthorized`, the client's identity is known to the server)
    
- 404 - Not Found
    
- 200 - OK
    
- 201 - Created
    
- 301 - Moved Permanently (New URL is given in the response)
    
- 302 -
    
- 308 - Permanent Redirect (he resource is now permanently located at another URI, specified by the `Location:` HTTP Response header)
    

D) List some **problems or challenges** you should consider when updating your API. What's the safest way to avoid these problems?

---

# **1. Marketplace(OfferUp)**

## requirements:

## **resource model:**

product (getProductInfo)

offer (giveOffer, acceptOffer, rejectOffer, cancelOffer)

buyer (getBuyerInfo, addBuyer, modifyBuyerInfo)

seller (getSellerInfo, addSeller, modifySellerInfo)

## **API:**

**getProductInfo**

```jsx
GET api/v1/marketplace/products/{productid}

with res:
	body = {"productid" : "23423", "price": "", "thumbnail": "<https://asd/asd.jpeg>",
	    "image1" : "<https://asd/asd2.jpeg>"}
	statusCode = [
		[200], 
		[400], 
		[401], 
		[403],  
	  [404, "Not found"]  
	]
```

**giveOffer**

```jsx
POST marketplace/products/{productid}/offers
with req:
	body = { "buyerid": "23423", "offer_price": "120"}
	
with res:
	body = { "offerid": "123" }
	statusCode = [ 
		[200], 
		[400], 
		[401], 
		[403],  
	  [404, "Not found"]  
	]
```

**acceptOffer**

```jsx
POST marketplace/products/{productid}/offers/{offerid}
with req:
	
with res:
	body = { "status": "pending" }
	statusCode = [ 
		[200], 
		[400], 
		[401], 
		[403],  
	  [404, "Not found"]  
	]
```

**rejectOffer**

```jsx
POST marketplace/products/{productid}/offers/{offerid}
with req:
	
with res:
	body = { "status": "pending" }
	statusCode = [ 
		[200], 
		[400], 
		[401], 
		[403],  
	  [404, "Not found"]  
	]
```

**cancelOffer**

```jsx
POST marketplace/products/{productid}/offers/{offerid}
with req:
	
with res:
	body = { "status": "pending" }
	statusCode = [ 
		[200], 
		[400], 
		[401], 
		[403],  
	  [404, "Not found"]  
	]
```

## OOAD

## NFR

## HLD

## Capacity Planning

## Scaling

## Deep Down

# 2. Spotify

## Functional Requirements

1. user logs in
    1. anonymous user can also listen
2. user selects a station ← stream of music (quality based on latency)
3. user selects song ← stream of music
4. user selects playlist
5. user create playlist (custom name
6. user add song to playlist
7. user view artist info (album, songs, artist info)

# 3. Homework Platform

# 4. Design an API resource model for facilitating checkout for a retail store.

An order captures product or service, price, and quantity information, besides other contextual details.

- Alternative
    
    POST /shoppingcart/products
    
    req= {product_id, quantity}
    
    → cart_id
    
    POST /checkout/{cart_id}
    

This was an Amazon Interview Question, by the way!!

**model**

[nouns]

- user_id
- product/service, price, quantity
- locale (currency, store_location)
- shipping? - maybe a separate entity

order

inventory, product, item(instance of product),

deliver, refunded, return, cancellation

[verb]

- checkout

**resource/endpoints**

```
POST /checkout
header = { some }
request = {
		 # could be flexible?
     stores: { "store_loc": "UK", "store_id": "123123", "currency": "BSP" }
     checkout_items: [{"user_id": "zhsd12", "product": "12340d212", "price": "123.23", "quantity": "1"}, {...}]
}
response
- status_code = [
     ("201", "created"),
     ("302", "redirect") # along with location header pointing to the payment processor
                         #  (inc. transaction ID, or token as a query paramenter)
     ("400", "malformed requests"), # body format is incorrect
     ("401", "authentication"),     # executed by anonymous user
     ("403", "forbidden"),          # payment information is not available?
     ("404", "not found"),          # product is not available
]
- header = {location: <https://paymentprocessor.com/id=sdfsd>}
- body = {
 # in case of any error, this contains error details
} 
```

### Discuss

- Chatty interactions vs. Fatty (which may be limiting)
- If someone wants to return order, how would you do it?
    - partially return,
- Good API designer should not assume how the API will be used

# 5. Design an API to provide current, historical, and forecasted weather.

[https://uplevel.interviewkickstart.com/resource/rc-freeform-711270-1132238-1066-6696](https://uplevel.interviewkickstart.com/resource/rc-freeform-711270-1132238-1066-6696)

### Modeling

Get

- Current
    
- Historical (Historic Duration, 3, 7, 10, 30)
    
- Forecast (Future Duration, 3, 7, 10, 30)
    
- Based on
    
    - Location in City/State/Country or Latitude/Logitude
    - DateTime
- Provide datapoints
    
- Update datapoints
    
- Delete datapoints
    
- Based on
    
    - Location in City/State/Country or Latitude/Logitude
    - DateTime (More granular)

### Endpoints

```python
GET api/v1/weather/current?location={}
- status_code = [
	("200", "OK"),          
	("400", "Bad Request"), # malformed query strings
	("404", "Not Found"),   # location not found, or, data not available for the location
]
- resp = {
	"avg_temperature"
}

GET api/v1/weather/historical?duration=3
- status_code = [
	("200", "OK"),          
	("400", "Bad Request"), # malformed query strings
	("404", "Not Found"),   # location not found, or, data not available for the location
]
- resp = {
	"avg_temperature"
}

GET api/v1/weather/forecast?duration=7

```

```python
GET api/v1/weather/admin/datapoints?location={xxx}&datetime={xxx}
- resp = {"datapoint_id": "sf234as", "time":"21/02/28-05:20:23", "temperature": 45, ...}

POST api/v1/weather/admin/datapoints
- req: 
- status_code: [
	("201", "Created")
]
- resp = [
]

PUT api/v1/weather/admin/datapoints/{datapoint_id}

DELETE api/v1/weather/admin/datapoints/{datapoint_id}
```

`

## Discussion

[https://uplevel.interviewkickstart.com/resource/helpful-class-video-694542-926-18147-0](https://uplevel.interviewkickstart.com/resource/helpful-class-video-694542-926-18147-0)

### Endpoints

**Compare these two choices**

```python
[Choice 1]

/weather/current
/weather/forcast
/weather/historical
```

vs.

```python
[Choice 2]

/current
/forecast
/historical
```

Generally speaking,

- General to specific, so, choice 1
- But, depends on the context
    - For example, if we need to get data for not only weather, but, stock price, various economic indicators, then choice 2 may make sense

### Location

```python
[Choice 1] GET with request body

{
	"city": ...,
	"state": ..., 
	"country": ..., 
}
```

- Notes on HTTP GET
    
    [HTTP GET with request body](https://stackoverflow.com/questions/978061/http-get-with-request-body)
    
    - The original HTTP/1.1 says not to use request body with HTTP GET
    - The revised RFC 7230-27237 says you can use use request body with HTTP GET, if there is a good reason. Elastic Search is an example of such. However, it is still advisable not to use since some implementation may not be ready with this. For example, many rest client won’t support this, but, curl does.
    - If you can use query string, you should use them
    - What about POST? POST is not idempotent, leading to request retry hesitancy.
        - The fix: Just because POST is not defined to be idempotent doesn't mean it mustn't be.
    - READ MORE about the topics in Stackoverflow.

```python
[Choice 2] Query String

/weather/current?city=""&state=""&country=""
```

```python
[Choice 3] Query String with Location as a resouce

GET /location?city=""&state=""&country=""
{
	"locationId": "12331"
}

GET /weather/current?locationId="12331"
```

```python
[Choice 4] Location as a resouce

GET /weather/forecast/{country}/{state}/{city}
e.g. /weather/forecast/US/WA/Seattle

GET/weather/forecast/{longitude}/{latitude}
e.g. /weather/forecast/37.2/122.9

or use separator
GET/weather/forecast/{logitude_latitude}
e.g. /weather/forecast/37.2:122.9

```

- We have fairly short list of query string and this doesn’t required to be encrypted, so, query string is a good choice, in this case.

# 6.

A) Which of these auth methods can you use to:

- Ensure only the blog's admin can write posts
- Allow marketplace moderators to remove non-compliant items
- Allow teachers to create new homework
- Allow sellers to mark their items as sold

_(Available Options: Access Control List, Role-Based Access Control, or Attribute-Based Access Control)_

B) For each of the scenarios mentioned, describe who would have access to what resources, and how would you check if that user has access to the described resource. Remember that you only need to take into consideration the endpoints that you listed in a previous question.

- Marketplace
- Playlists
- Homeworks

C) Write 3 endpoints using Basic Auth or another type of authentication, and demonstrate the 3 different types of access control discussed in class. You can generate a list with fake data for these scenarios:

- Access Control List: Let listed admins delete any marketplace item.
- Role-Based Access Control: Let teachers create the homework, but not students
- Attribute-based Access Control: Let marketplace item owners edit or delete their items.