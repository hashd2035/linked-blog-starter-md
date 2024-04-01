---
icon: luc_monitor
---
```toc
```

# Introduction
- Introduce yourself
- Behavioral Question

# Exercise
[[URL Shortener - 1. First Try]]

## Lesson Learned and To Do Next
- [ ] Let's think about what consistency means
- [ ] How does auth token header look like
	- [ ] browser-based vs. API token, etc.
	- [ ] cookie 
- [ ] How does client's side session management happens and impact on REST calls
- [ ] How to specify ttl on header (formatting) and how to control
- [ ] How to cache on browser and how to control 
- [ ] How does cache works on requests and how to control 

- [ ] how big is long url? (data size), twits, one page texts, a book, etc.     
- [ ] More fluent capacity planning


3:00
# Functional Requirements
- Creator creates Shortened URL (long URL)
	- Expiry Time, Custom domain/Custom URL, Unique URL  
	- Analytics, Admin Features (Update, Delete)
	- Login (or Authenticate)
- System on behalf of Consumers 
	- redirect shortened URL to long URL
- Rate Limiting on creation
# Non Functional Requirements
* High availability (Over consistency)
* Low Latency
* Scalability
* Reliability
# Capacity Planning
* Traffic (let's check the reference)
	* 100 million DAU 
	* 1:100 read/write ratio => 1million writes / 100 million reads per day
	* 8000 concurrent requests/server 
* Storage
	* avg_size of long URL = 5k 
# API Design
REST API makes sense as this will be customer facing and browser based
- [ ] Find out what authentication methods are appropriate for
	- [ ] Browser based REST access
	- [ ] API call by system
- [ ] Find out what's the standard for expressing TTL or expiration_time 

```
POST /api/v1/short_url 
header = {auth: XXX}
{
	"long_url": "...", 
	"expire_by": "...", 
	"custom_name": "..."
}
status_codes = {
	[201, "created"], 
	[401, "malformat"], 
	[404, "notfound - custom_name not found"], 
}
```

```
GET http://bit.ly/sh12as
header = {location: "https://orignal_long_url"}
status_codes = {
	[302, "redirect"], 
	[304, "Not Found"], 
}
```
3:16
# HLD
![[URL Shortener 2024-03-28 15.16.36.excalidraw]]

[[Storage Choice]]
[[Redirecting Shortened URLs]]
# Deep Down Topics

[[Shortened URL Generation]]


# Scaling



# Wrap Up
