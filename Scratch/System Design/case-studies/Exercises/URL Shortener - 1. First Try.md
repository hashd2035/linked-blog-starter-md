---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
3:23, 3:41

[FR]
1. Creator shortens URL (Custom Name, Custom domain, TTL) 
  - not be predictable
2. Consumer hits Short URL
   - gets redirected

- Admin (update/delete urls/Analytics)
- Login / Anonymous

read: write = 200:1 


[NFR]
1. High availability over strong consistency for consumer
2. Consistency over availability for creator 
3. Reliability (shortened url / long url should not be broken)
4. Scalability/Elasticity 
5. Low latency

3:45 ~ 4:02
[API]
1. POST api/v1/shortenedURL
header = {auth_token}
{
    "custom_name": "arj131", 
    "custon_domain": "www.james.com", 
    "ttl"      :
}
status_code: [
    201: created, 
    404: not found, # long url does not exists
    401?: malformatted 
    402/403?: Unauthorized, forbidden               
]
response: {
    shortened_url: "arj131"
}

2. GET https://ads.com/arj131
status_code: [ 
    302: temp redirect
    404: Not found
]







 ^XFKjBxKv

- Let's think about what consistency means
- How does auth token header look like
  browser-based vs. API token, etc.
  cookie 
- How does client's side session management happens and impact on REST calls
- How to specify ttl on header (formatting) and how to control
- How to cache on browser and how to control 
- How does cache works on requests and how to control 

- how big is long url? (data size), twits, one page texts, a book, etc.     
- More fluent capacity planning
- Cache - Caching strategy
    
      ^5cO1CE4F

1. POST api/v1/shortenedURL ^qMmM8Xc2

K/V db ^JGInDuuH

302
location: long_url ^Gkc6Kf2P

Long_url ^IqF2QMhp

Short_url ^tvKBk06t

2. GET https://ads.com/arj131 ^pTWkTFN3

[stateless server]

200 million DAU
r:w = 100: 1
creates 1 url per day
==================
worst case request per sec
200mil rps / 10k = 20,000 for writes
2,000,000 = 2 million servers for reads
================== ^QLpK2s8H

[storage]

1k for  ^AQwSfqpQ

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.25",
	"elements": [
		{
			"type": "text",
			"version": 1225,
			"versionNonce": 164015063,
			"isDeleted": false,
			"id": "XFKjBxKv",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1390,
			"y": -946.2421875,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 622.0795288085938,
			"height": 1325,
			"seed": 675422105,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148536658,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "3:23, 3:41\n\n[FR]\n1. Creator shortens URL (Custom Name, Custom domain, TTL) \n  - not be predictable\n2. Consumer hits Short URL\n   - gets redirected\n\n- Admin (update/delete urls/Analytics)\n- Login / Anonymous\n\nread: write = 200:1 \n\n\n[NFR]\n1. High availability over strong consistency for consumer\n2. Consistency over availability for creator \n3. Reliability (shortened url / long url should not be broken)\n4. Scalability/Elasticity \n5. Low latency\n\n3:45 ~ 4:02\n[API]\n1. POST api/v1/shortenedURL\nheader = {auth_token}\n{\n    \"custom_name\": \"arj131\", \n    \"custon_domain\": \"www.james.com\", \n    \"ttl\"      :\n}\nstatus_code: [\n    201: created, \n    404: not found, # long url does not exists\n    401?: malformatted \n    402/403?: Unauthorized, forbidden               \n]\nresponse: {\n    shortened_url: \"arj131\"\n}\n\n2. GET https://ads.com/arj131\nstatus_code: [ \n    302: temp redirect\n    404: Not found\n]\n\n\n\n\n\n\n\n",
			"rawText": "3:23, 3:41\n\n[FR]\n1. Creator shortens URL (Custom Name, Custom domain, TTL) \n  - not be predictable\n2. Consumer hits Short URL\n   - gets redirected\n\n- Admin (update/delete urls/Analytics)\n- Login / Anonymous\n\nread: write = 200:1 \n\n\n[NFR]\n1. High availability over strong consistency for consumer\n2. Consistency over availability for creator \n3. Reliability (shortened url / long url should not be broken)\n4. Scalability/Elasticity \n5. Low latency\n\n3:45 ~ 4:02\n[API]\n1. POST api/v1/shortenedURL\nheader = {auth_token}\n{\n    \"custom_name\": \"arj131\", \n    \"custon_domain\": \"www.james.com\", \n    \"ttl\"      :\n}\nstatus_code: [\n    201: created, \n    404: not found, # long url does not exists\n    401?: malformatted \n    402/403?: Unauthorized, forbidden               \n]\nresponse: {\n    shortened_url: \"arj131\"\n}\n\n2. GET https://ads.com/arj131\nstatus_code: [ \n    302: temp redirect\n    404: Not found\n]\n\n\n\n\n\n\n\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "3:23, 3:41\n\n[FR]\n1. Creator shortens URL (Custom Name, Custom domain, TTL) \n  - not be predictable\n2. Consumer hits Short URL\n   - gets redirected\n\n- Admin (update/delete urls/Analytics)\n- Login / Anonymous\n\nread: write = 200:1 \n\n\n[NFR]\n1. High availability over strong consistency for consumer\n2. Consistency over availability for creator \n3. Reliability (shortened url / long url should not be broken)\n4. Scalability/Elasticity \n5. Low latency\n\n3:45 ~ 4:02\n[API]\n1. POST api/v1/shortenedURL\nheader = {auth_token}\n{\n    \"custom_name\": \"arj131\", \n    \"custon_domain\": \"www.james.com\", \n    \"ttl\"      :\n}\nstatus_code: [\n    201: created, \n    404: not found, # long url does not exists\n    401?: malformatted \n    402/403?: Unauthorized, forbidden               \n]\nresponse: {\n    shortened_url: \"arj131\"\n}\n\n2. GET https://ads.com/arj131\nstatus_code: [ \n    302: temp redirect\n    404: Not found\n]\n\n\n\n\n\n\n\n",
			"lineHeight": 1.25,
			"baseline": 1318
		},
		{
			"type": "text",
			"version": 806,
			"versionNonce": 179145497,
			"isDeleted": false,
			"id": "5cO1CE4F",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -466.5490056693116,
			"y": -1009.7615006097121,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 784.139404296875,
			"height": 350,
			"seed": 1063333241,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711231171674,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "- Let's think about what consistency means\n- How does auth token header look like\n  browser-based vs. API token, etc.\n  cookie \n- How does client's side session management happens and impact on REST calls\n- How to specify ttl on header (formatting) and how to control\n- How to cache on browser and how to control \n- How does cache works on requests and how to control \n\n- how big is long url? (data size), twits, one page texts, a book, etc.     \n- More fluent capacity planning\n- Cache - Caching strategy\n    \n     ",
			"rawText": "- Let's think about what consistency means\n- How does auth token header look like\n  browser-based vs. API token, etc.\n  cookie \n- How does client's side session management happens and impact on REST calls\n- How to specify ttl on header (formatting) and how to control\n- How to cache on browser and how to control \n- How does cache works on requests and how to control \n\n- how big is long url? (data size), twits, one page texts, a book, etc.     \n- More fluent capacity planning\n- Cache - Caching strategy\n    \n     ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- Let's think about what consistency means\n- How does auth token header look like\n  browser-based vs. API token, etc.\n  cookie \n- How does client's side session management happens and impact on REST calls\n- How to specify ttl on header (formatting) and how to control\n- How to cache on browser and how to control \n- How does cache works on requests and how to control \n\n- how big is long url? (data size), twits, one page texts, a book, etc.     \n- More fluent capacity planning\n- Cache - Caching strategy\n    \n     ",
			"lineHeight": 1.25,
			"baseline": 343
		},
		{
			"type": "text",
			"version": 104,
			"versionNonce": 1013394071,
			"isDeleted": false,
			"id": "qMmM8Xc2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -612.8640817495493,
			"y": -555.4843749999999,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 284.47979736328125,
			"height": 25,
			"seed": 1431119449,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148483430,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "1. POST api/v1/shortenedURL",
			"rawText": "1. POST api/v1/shortenedURL",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1. POST api/v1/shortenedURL",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "ellipse",
			"version": 26,
			"versionNonce": 64252025,
			"isDeleted": false,
			"id": "k5TDItZGZpf7b9Wpe0tx9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -579.2743381598061,
			"y": -462.971554487179,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 101.53846153846166,
			"height": 90.76923076923083,
			"seed": 675191097,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "Zm3etVK59enWu0aZfqD-G",
					"type": "arrow"
				}
			],
			"updated": 1711148466192,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 50,
			"versionNonce": 543111063,
			"isDeleted": false,
			"id": "Hn3mVt-mbmAJFW_jVa6Pq",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -214.65895354442137,
			"y": -495.27924679487126,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 150.76923076923094,
			"height": 115.38461538461547,
			"seed": 315817529,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "Zm3etVK59enWu0aZfqD-G",
					"type": "arrow"
				},
				{
					"id": "Wzq5dPzlIBzUVSq5C8l5T",
					"type": "arrow"
				}
			],
			"updated": 1711148466192,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 35,
			"versionNonce": 33747289,
			"isDeleted": false,
			"id": "Zm3etVK59enWu0aZfqD-G",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -463.88972277519065,
			"y": -418.35616987179435,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 227.69230769230785,
			"height": 6.153846153846075,
			"seed": 400476217,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711148466192,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "k5TDItZGZpf7b9Wpe0tx9",
				"focus": 0.021520171334524066,
				"gap": 13.851590375938933
			},
			"endBinding": {
				"elementId": "Hn3mVt-mbmAJFW_jVa6Pq",
				"focus": -0.17507831534980942,
				"gap": 21.538461538461434
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					227.69230769230785,
					-6.153846153846075
				]
			]
		},
		{
			"type": "rectangle",
			"version": 317,
			"versionNonce": 983298071,
			"isDeleted": false,
			"id": "hJmlXdDYbIWWHV1a4IfGp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 239.18720030173267,
			"y": -458.35616987179435,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 155.38461538461547,
			"height": 130.76923076923083,
			"seed": 1975972663,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "JGInDuuH"
				},
				{
					"id": "Wzq5dPzlIBzUVSq5C8l5T",
					"type": "arrow"
				},
				{
					"id": "MeH2sC_5efOaji4svMx6o",
					"type": "arrow"
				},
				{
					"id": "CjsTLAXHyfUZNveLjFtYI",
					"type": "arrow"
				}
			],
			"updated": 1711149050268,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 267,
			"versionNonce": 1542706487,
			"isDeleted": false,
			"id": "JGInDuuH",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 284.80952355800525,
			"y": -405.47155448717893,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 64.13996887207031,
			"height": 25,
			"seed": 2112380183,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711149050268,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "K/V db",
			"rawText": "K/V db",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hJmlXdDYbIWWHV1a4IfGp",
			"originalText": "K/V db",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "arrow",
			"version": 179,
			"versionNonce": 876346039,
			"isDeleted": false,
			"id": "Wzq5dPzlIBzUVSq5C8l5T",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -45.42818431365207,
			"y": -449.8593630669756,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 273.84615384615427,
			"height": 34.76527108366338,
			"seed": 1528101751,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711231164480,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Hn3mVt-mbmAJFW_jVa6Pq",
				"gap": 18.46153846153834,
				"focus": -0.3598040479566842
			},
			"endBinding": {
				"elementId": "hJmlXdDYbIWWHV1a4IfGp",
				"gap": 10.76923076923049,
				"focus": 0.14475085808971525
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					273.84615384615427,
					34.76527108366338
				]
			]
		},
		{
			"type": "ellipse",
			"version": 56,
			"versionNonce": 1508239737,
			"isDeleted": false,
			"id": "-MjofEyidl24ctaETV5ma",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -586.966645852114,
			"y": -224.51001602564043,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 109.23076923076928,
			"height": 93.84615384615392,
			"seed": 203337207,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "wXWtmjOmMjZFfaSgXnFMG",
					"type": "arrow"
				},
				{
					"id": "fnprCy5Z4RhPnxAz7wWSR",
					"type": "arrow"
				},
				{
					"id": "00MrTebqR80y4I1aIeBGe",
					"type": "arrow"
				}
			],
			"updated": 1711148476757,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 93,
			"versionNonce": 249710231,
			"isDeleted": false,
			"id": "Th6Jat3w9DaLt8q_0CwPD",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -223.88972277519065,
			"y": -239.89463141025578,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 166.1538461538462,
			"height": 126.15384615384619,
			"seed": 364810359,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "wXWtmjOmMjZFfaSgXnFMG",
					"type": "arrow"
				},
				{
					"id": "MeH2sC_5efOaji4svMx6o",
					"type": "arrow"
				},
				{
					"id": "CjsTLAXHyfUZNveLjFtYI",
					"type": "arrow"
				},
				{
					"id": "fnprCy5Z4RhPnxAz7wWSR",
					"type": "arrow"
				}
			],
			"updated": 1711148476757,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 51,
			"versionNonce": 2084328025,
			"isDeleted": false,
			"id": "wXWtmjOmMjZFfaSgXnFMG",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -471.5820304674985,
			"y": -201.43309294871733,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 233.84615384615404,
			"height": 4.615384615384642,
			"seed": 12772215,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711148476757,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "-MjofEyidl24ctaETV5ma",
				"focus": -0.4825085925049961,
				"gap": 11.851949307791983
			},
			"endBinding": {
				"elementId": "Th6Jat3w9DaLt8q_0CwPD",
				"focus": 0.4812324053800446,
				"gap": 13.846153846153811
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					233.84615384615404,
					-4.615384615384642
				]
			]
		},
		{
			"type": "arrow",
			"version": 115,
			"versionNonce": 422050039,
			"isDeleted": false,
			"id": "MeH2sC_5efOaji4svMx6o",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -42.351261236729016,
			"y": -218.57908643560572,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 272.3076923076924,
			"height": 150.83931858225802,
			"seed": 836147129,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711231164480,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Th6Jat3w9DaLt8q_0CwPD",
				"gap": 15.384615384615472,
				"focus": 0.11693498065643468
			},
			"endBinding": {
				"elementId": "hJmlXdDYbIWWHV1a4IfGp",
				"gap": 9.230769230769283,
				"focus": 0.2268582136164907
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					272.3076923076924,
					-150.83931858225802
				]
			]
		},
		{
			"type": "arrow",
			"version": 127,
			"versionNonce": 827942711,
			"isDeleted": false,
			"id": "CjsTLAXHyfUZNveLjFtYI",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 225.34104645557886,
			"y": -339.7779454167887,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 267.69230769230785,
			"height": 156.79896938426882,
			"seed": 13080215,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711231164481,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "hJmlXdDYbIWWHV1a4IfGp",
				"gap": 13.846153846153811,
				"focus": 0.003861003861003578
			},
			"endBinding": {
				"elementId": "Th6Jat3w9DaLt8q_0CwPD",
				"gap": 15.384615384615472,
				"focus": 0.4610034773969203
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-267.69230769230785,
					156.79896938426882
				]
			]
		},
		{
			"type": "arrow",
			"version": 52,
			"versionNonce": 841702327,
			"isDeleted": false,
			"id": "fnprCy5Z4RhPnxAz7wWSR",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -242.351261236729,
			"y": -189.12540064102495,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 227.69230769230785,
			"height": 3.0769230769230944,
			"seed": 215031449,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711148476757,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Th6Jat3w9DaLt8q_0CwPD",
				"focus": 0.2130829015544035,
				"gap": 18.46153846153834
			},
			"endBinding": {
				"elementId": "-MjofEyidl24ctaETV5ma",
				"focus": -0.16236361231620344,
				"gap": 8.43109866194537
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-227.69230769230785,
					3.0769230769230944
				]
			]
		},
		{
			"type": "text",
			"version": 63,
			"versionNonce": 1569890105,
			"isDeleted": false,
			"id": "Gkc6Kf2P",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -430.04356892903684,
			"y": -178.35616987179424,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 168.099853515625,
			"height": 50,
			"seed": 853683287,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148476757,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "302\nlocation: long_url",
			"rawText": "302\nlocation: long_url",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "302\nlocation: long_url",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "arrow",
			"version": 55,
			"versionNonce": 1909771479,
			"isDeleted": false,
			"id": "00MrTebqR80y4I1aIeBGe",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -496.197415082883,
			"y": -124.51001602564031,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 430.76923076923094,
			"height": 363.0769230769233,
			"seed": 210739673,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1711148476757,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "-MjofEyidl24ctaETV5ma",
				"focus": 0.3438827212533283,
				"gap": 15.115302138069154
			},
			"endBinding": {
				"elementId": "6aPO-kxhVR8BWSnaJeTFF",
				"focus": -1.0185918139906724,
				"gap": 18.62467435970987
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					430.76923076923094,
					363.0769230769233
				]
			]
		},
		{
			"type": "ellipse",
			"version": 58,
			"versionNonce": 1548505113,
			"isDeleted": false,
			"id": "6aPO-kxhVR8BWSnaJeTFF",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -46.96664585211374,
			"y": 153.95152243589848,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 487.69230769230785,
			"height": 161.53846153846143,
			"seed": 542126297,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "00MrTebqR80y4I1aIeBGe",
					"type": "arrow"
				}
			],
			"updated": 1711148476757,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 11,
			"versionNonce": 426973687,
			"isDeleted": false,
			"id": "IqF2QMhp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -406.96664585211374,
			"y": 66.25921474359063,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 84.15992736816406,
			"height": 25,
			"seed": 1470836633,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148476757,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Long_url",
			"rawText": "Long_url",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Long_url",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 16,
			"versionNonce": 1046275321,
			"isDeleted": false,
			"id": "tvKBk06t",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -426.96664585211374,
			"y": -224.51001602564043,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 94.75990295410156,
			"height": 25,
			"seed": 1808741465,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148476757,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Short_url",
			"rawText": "Short_url",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Short_url",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 117,
			"versionNonce": 1111960727,
			"isDeleted": false,
			"id": "pTWkTFN3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -622.3512612367297,
			"y": -269.12540064102507,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 300.8998107910156,
			"height": 25,
			"seed": 510983287,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148520188,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "2. GET https://ads.com/arj131",
			"rawText": "2. GET https://ads.com/arj131",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "2. GET https://ads.com/arj131",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 372,
			"versionNonce": 313489783,
			"isDeleted": false,
			"id": "QLpK2s8H",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 294.5718156863461,
			"y": -181.43309294871779,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 401.7996826171875,
			"height": 250,
			"seed": 1194798809,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711148897753,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[stateless server]\n\n200 million DAU\nr:w = 100: 1\ncreates 1 url per day\n==================\nworst case request per sec\n200mil rps / 10k = 20,000 for writes\n2,000,000 = 2 million servers for reads\n==================",
			"rawText": "[stateless server]\n\n200 million DAU\nr:w = 100: 1\ncreates 1 url per day\n==================\nworst case request per sec\n200mil rps / 10k = 20,000 for writes\n2,000,000 = 2 million servers for reads\n==================",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[stateless server]\n\n200 million DAU\nr:w = 100: 1\ncreates 1 url per day\n==================\nworst case request per sec\n200mil rps / 10k = 20,000 for writes\n2,000,000 = 2 million servers for reads\n==================",
			"lineHeight": 1.25,
			"baseline": 243
		},
		{
			"type": "text",
			"version": 52,
			"versionNonce": 947169337,
			"isDeleted": false,
			"id": "AQwSfqpQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 776.1102772248075,
			"y": -179.89463141025635,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 95.95991516113281,
			"height": 75,
			"seed": 1966809561,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711149040075,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[storage]\n\n1k for ",
			"rawText": "[storage]\n\n1k for ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[storage]\n\n1k for ",
			"lineHeight": 1.25,
			"baseline": 68
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1971c2",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 2,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 538.9255631807742,
		"scrollY": 1104.1974184415162,
		"zoom": {
			"value": 1.5402887284216236
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"gridColor": {
			"Bold": "#C9C9C9FF",
			"Regular": "#EDEDEDFF"
		},
		"currentStrokeOptions": null,
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%