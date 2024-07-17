---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
1. start indexing root URL
e.g. www.bettert.com ^norTB4a6

2. Ensure no duplication / 
Insert Url, runId, date, 
referringURL, rootURL ^Wuuzrupk

Lambda ^JLHcmfDU

3. Queue URL for crawling ^gmYH1UdD

4. Invoke Lambda from Queue to 
process the current URL ^nrik4kGf

5. Invoke docker that renders 
the page and scrapes the 
content ^qmWFXibA

8. Mark the current URL as visited
and also figure out which page links 
aren't visited yet ^WPS4kz44

9. Queue unvisited 
  URLs ^zFg12okO

Lambda ^759y94QN

DB ^AdUtnjpi

www.bettert.com ^QagwOHkm

s3 ^sw7MD4W9

dynamoDB ^zu86hR0J

lambda ^nRAuFgqJ

/products/daily-best ^h559n99i

6. Store images, videos, etc. in S3 and 
enable CloudFront for CDN access ^SVusP9hx

<<Render Pages>>
<<Scrape Content>> ^qYGDNl1a

6. Index product by search 
terms in Elastic Search ^kWloL9bw

7. Scrape and structure the content 
into MongoDB document storage. 
Refer to CDN urls from S3 ^2J6r7nmn

1. Access Page ^Tk3yhDjJ

2. Access CDN ^flHLBf0N

2. Check Cache ^AkueTOBc

3. Search product 
by search term ^fQKmaopa

4. Get product details and 
URLs cache results ^KVpFzqUU

Mongo
DB ^1tfrCAIA

S3 ^H48gAxQc

ES ^MD42Vpsf

CDN ^HBHazssv

svc ^gjmuADZ4

svc ^Czj4Q62c

cache ^YPAus0D8

SQS ^Xzf5jXuW

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.25",
	"elements": [
		{
			"type": "ellipse",
			"version": 31,
			"versionNonce": 659920022,
			"isDeleted": false,
			"id": "dufUYwEVuJAv311LKc0Jn",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 7,
			"y": -281.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 56,
			"height": 55,
			"seed": 935449686,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "7-kviq0H5gNMqZ-_4ySa2",
					"type": "arrow"
				}
			],
			"updated": 1712860694783,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 70,
			"versionNonce": 685631254,
			"isDeleted": false,
			"id": "3bWb5CvScXNg9wgERwlUE",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 0,
			"y": -189.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 72,
			"height": 74,
			"seed": 1164474262,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "-jTmtZJTYDwnvp-g_I0eP",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "Czj4Q62c"
				},
				{
					"id": "7-kviq0H5gNMqZ-_4ySa2",
					"type": "arrow"
				}
			],
			"updated": 1712860694783,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 4,
			"versionNonce": 1593165964,
			"isDeleted": false,
			"id": "Czj4Q62c",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 23.456008911132812,
			"y": -162.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 25.087982177734375,
			"height": 20,
			"seed": 1287685812,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712860053529,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "svc",
			"rawText": "svc",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3bWb5CvScXNg9wgERwlUE",
			"originalText": "svc",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 120,
			"versionNonce": 945755316,
			"isDeleted": false,
			"id": "7O6fy3MqETcWp-GZ3hUYr",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 0,
			"y": -66.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffd8a8",
			"width": 72,
			"height": 74,
			"seed": 1659506314,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "-jTmtZJTYDwnvp-g_I0eP",
					"type": "arrow"
				},
				{
					"id": "VxTVtnjNXJflbcsSm3Jva",
					"type": "arrow"
				},
				{
					"id": "A6tRthyGKnmxCDxphGHVr",
					"type": "arrow"
				},
				{
					"id": "XwO4-vFcj8g1izrMpF5wS",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "JLHcmfDU"
				}
			],
			"updated": 1712859951328,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 14,
			"versionNonce": 399992332,
			"isDeleted": false,
			"id": "JLHcmfDU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 6.85601806640625,
			"y": -39.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 58.2879638671875,
			"height": 20,
			"seed": 1791191766,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805253,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Lambda",
			"rawText": "Lambda",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7O6fy3MqETcWp-GZ3hUYr",
			"originalText": "Lambda",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 97,
			"versionNonce": 1000705460,
			"isDeleted": false,
			"id": "fE7pKGz5O2byqJ7OlicZ2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 0,
			"y": 55.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 72,
			"height": 74,
			"seed": 1784656662,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "VxTVtnjNXJflbcsSm3Jva",
					"type": "arrow"
				},
				{
					"id": "8u3ILZiiJ6OpVT8jRbqOn",
					"type": "arrow"
				},
				{
					"id": "WZ_SkOo7CyKRf7vBB0v_4",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "Xzf5jXuW"
				}
			],
			"updated": 1712860098526,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 9,
			"versionNonce": 1522549556,
			"isDeleted": false,
			"id": "Xzf5jXuW",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 20.632003784179688,
			"y": 82.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 30.735992431640625,
			"height": 20,
			"seed": 713120012,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712860105717,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "SQS",
			"rawText": "SQS",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fE7pKGz5O2byqJ7OlicZ2",
			"originalText": "SQS",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 97,
			"versionNonce": 1263595956,
			"isDeleted": false,
			"id": "rrxxae2o_PsOckcuEc6oU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 0,
			"y": 218.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffd8a8",
			"width": 72,
			"height": 74,
			"seed": 1024327242,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "8u3ILZiiJ6OpVT8jRbqOn",
					"type": "arrow"
				},
				{
					"id": "WZ_SkOo7CyKRf7vBB0v_4",
					"type": "arrow"
				},
				{
					"id": "6ZB0UDdHPNmLJLiPRMcV-",
					"type": "arrow"
				},
				{
					"id": "Ne-JKx6eromcIsJM7q-ZU",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "759y94QN"
				},
				{
					"id": "8lgqLQdvaioi9il7dS30k",
					"type": "arrow"
				}
			],
			"updated": 1712859945988,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 6,
			"versionNonce": 915315252,
			"isDeleted": false,
			"id": "759y94QN",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 6.85601806640625,
			"y": 245.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 58.2879638671875,
			"height": 20,
			"seed": 2035941654,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805253,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Lambda",
			"rawText": "Lambda",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rrxxae2o_PsOckcuEc6oU",
			"originalText": "Lambda",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 90,
			"versionNonce": 1734037388,
			"isDeleted": false,
			"id": "oCooVThVTznBuCp3P_eL3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 207,
			"y": -59.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 72,
			"height": 74,
			"seed": 1013301590,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "A6tRthyGKnmxCDxphGHVr",
					"type": "arrow"
				},
				{
					"id": "XwO4-vFcj8g1izrMpF5wS",
					"type": "arrow"
				},
				{
					"id": "6ZB0UDdHPNmLJLiPRMcV-",
					"type": "arrow"
				},
				{
					"id": "Ne-JKx6eromcIsJM7q-ZU",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "AdUtnjpi"
				}
			],
			"updated": 1712859991534,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 7,
			"versionNonce": 329593780,
			"isDeleted": false,
			"id": "AdUtnjpi",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 230.94400787353516,
			"y": -32.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 24.111984252929688,
			"height": 20,
			"seed": 397646550,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805253,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "DB",
			"rawText": "DB",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "oCooVThVTznBuCp3P_eL3",
			"originalText": "DB",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "arrow",
			"version": 52,
			"versionNonce": 450954122,
			"isDeleted": false,
			"id": "-jTmtZJTYDwnvp-g_I0eP",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 39,
			"y": -106.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 0,
			"height": 38,
			"seed": 2063112650,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165533,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "3bWb5CvScXNg9wgERwlUE",
				"gap": 9,
				"focus": -0.08333333333333333
			},
			"endBinding": {
				"elementId": "7O6fy3MqETcWp-GZ3hUYr",
				"gap": 2,
				"focus": 0.08333333333333333
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
					0,
					38
				]
			]
		},
		{
			"type": "arrow",
			"version": 42,
			"versionNonce": 1482512778,
			"isDeleted": false,
			"id": "VxTVtnjNXJflbcsSm3Jva",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 39,
			"y": 18.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 0,
			"height": 30,
			"seed": 1317250454,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165540,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "7O6fy3MqETcWp-GZ3hUYr",
				"gap": 11,
				"focus": -0.08333333333333333
			},
			"endBinding": {
				"elementId": "fE7pKGz5O2byqJ7OlicZ2",
				"gap": 7,
				"focus": 0.08333333333333333
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
					0,
					30
				]
			]
		},
		{
			"type": "arrow",
			"version": 239,
			"versionNonce": 627188554,
			"isDeleted": false,
			"id": "8u3ILZiiJ6OpVT8jRbqOn",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 34.22269219026318,
			"y": 142.50686160873238,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 0.7754231636952369,
			"height": 63.81831014770677,
			"seed": 1852238218,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165545,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "fE7pKGz5O2byqJ7OlicZ2",
				"gap": 12.530299108732379,
				"focus": 0.03224978850222771
			},
			"endBinding": {
				"elementId": "rrxxae2o_PsOckcuEc6oU",
				"gap": 12.65139074356091,
				"focus": -0.08658591701235123
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
					-0.7754231636952369,
					63.81831014770677
				]
			]
		},
		{
			"type": "arrow",
			"version": 90,
			"versionNonce": 1867684490,
			"isDeleted": false,
			"id": "A6tRthyGKnmxCDxphGHVr",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 79.00000000000001,
			"y": -27.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 119.00000000000001,
			"height": 2,
			"seed": 1380487126,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165547,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "7O6fy3MqETcWp-GZ3hUYr",
				"gap": 7,
				"focus": 0.0724022346368715
			},
			"endBinding": {
				"elementId": "oCooVThVTznBuCp3P_eL3",
				"gap": 9,
				"focus": 0.20625698324022346
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
					119.00000000000001,
					-2
				]
			]
		},
		{
			"type": "arrow",
			"version": 67,
			"versionNonce": 614531082,
			"isDeleted": false,
			"id": "XwO4-vFcj8g1izrMpF5wS",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 195,
			"y": -15.023437499999998,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 117,
			"height": 1.9999999999999982,
			"seed": 1355209354,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165547,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "oCooVThVTznBuCp3P_eL3",
				"gap": 12,
				"focus": -0.16428084526244038
			},
			"endBinding": {
				"elementId": "7O6fy3MqETcWp-GZ3hUYr",
				"gap": 6,
				"focus": 0.44444444444444453
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
					-117,
					1.9999999999999982
				]
			]
		},
		{
			"type": "arrow",
			"version": 180,
			"versionNonce": 1083386378,
			"isDeleted": false,
			"id": "WZ_SkOo7CyKRf7vBB0v_4",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 79,
			"y": 242.9765625,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 56,
			"height": 156,
			"seed": 1904562506,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165545,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "rrxxae2o_PsOckcuEc6oU",
				"gap": 7,
				"focus": 0.565934065934066
			},
			"endBinding": {
				"elementId": "fE7pKGz5O2byqJ7OlicZ2",
				"gap": 8,
				"focus": -0.7559974065269074
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
					56,
					-84
				],
				[
					1,
					-156
				]
			]
		},
		{
			"type": "arrow",
			"version": 104,
			"versionNonce": 1431858890,
			"isDeleted": false,
			"id": "6ZB0UDdHPNmLJLiPRMcV-",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 241.00000000000003,
			"y": 23.9765625,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 163.00000000000003,
			"height": 236,
			"seed": 187813846,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165547,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "oCooVThVTznBuCp3P_eL3",
				"gap": 9,
				"focus": -0.040748162992651965
			},
			"endBinding": {
				"elementId": "rrxxae2o_PsOckcuEc6oU",
				"gap": 6,
				"focus": 0.4740601944021549
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
					-12.000000000000028,
					154
				],
				[
					-163.00000000000003,
					236
				]
			]
		},
		{
			"type": "arrow",
			"version": 370,
			"versionNonce": 1119094154,
			"isDeleted": false,
			"id": "Ne-JKx6eromcIsJM7q-ZU",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 86.68038051194304,
			"y": 273.5065131990519,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 165,
			"height": 246.00000000000006,
			"seed": 775367946,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165548,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "rrxxae2o_PsOckcuEc6oU",
				"gap": 14.680380511943042,
				"focus": 0.8230594474307841
			},
			"endBinding": {
				"elementId": "oCooVThVTznBuCp3P_eL3",
				"gap": 12.529950699051824,
				"focus": -0.2916746134043884
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
					158,
					-97.00000000000006
				],
				[
					165,
					-246.00000000000006
				]
			]
		},
		{
			"type": "text",
			"version": 58,
			"versionNonce": 685042572,
			"isDeleted": false,
			"id": "norTB4a6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -253,
			"y": -175.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 207.35987854003906,
			"height": 40,
			"seed": 360316234,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "1. start indexing root URL\ne.g. www.bettert.com",
			"rawText": "1. start indexing root URL\ne.g. www.bettert.com",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1. start indexing root URL\ne.g. www.bettert.com",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "text",
			"version": 112,
			"versionNonce": 736781108,
			"isDeleted": false,
			"id": "Wuuzrupk",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -254,
			"y": -63.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 213.1519012451172,
			"height": 60,
			"seed": 1910545046,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "2. Ensure no duplication / \nInsert Url, runId, date, \nreferringURL, rootURL",
			"rawText": "2. Ensure no duplication / \nInsert Url, runId, date, \nreferringURL, rootURL",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "2. Ensure no duplication / \nInsert Url, runId, date, \nreferringURL, rootURL",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "text",
			"version": 34,
			"versionNonce": 684169740,
			"isDeleted": false,
			"id": "gmYH1UdD",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -253,
			"y": 63.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 208.14389038085938,
			"height": 20,
			"seed": 789107466,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "3. Queue URL for crawling",
			"rawText": "3. Queue URL for crawling",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "3. Queue URL for crawling",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 96,
			"versionNonce": 1553980596,
			"isDeleted": false,
			"id": "nrik4kGf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -259.266984023737,
			"y": 152.78764716468856,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 269.391845703125,
			"height": 40,
			"seed": 1611171210,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "8u3ILZiiJ6OpVT8jRbqOn",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "4. Invoke Lambda from Queue to \nprocess the current URL",
			"rawText": "4. Invoke Lambda from Queue to \nprocess the current URL",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "4. Invoke Lambda from Queue to \nprocess the current URL",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "text",
			"version": 72,
			"versionNonce": 593524876,
			"isDeleted": false,
			"id": "qmWFXibA",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -257,
			"y": 228.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 246.84783935546875,
			"height": 60,
			"seed": 1943852874,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "5. Invoke docker that renders \nthe page and scrapes the \ncontent",
			"rawText": "5. Invoke docker that renders \nthe page and scrapes the \ncontent",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "5. Invoke docker that renders \nthe page and scrapes the \ncontent",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "text",
			"version": 103,
			"versionNonce": 459941428,
			"isDeleted": false,
			"id": "WPS4kz44",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 296.21739130434776,
			"y": -48.82642663043481,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 290.767822265625,
			"height": 60,
			"seed": 1168248662,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "8. Mark the current URL as visited\nand also figure out which page links \naren't visited yet",
			"rawText": "8. Mark the current URL as visited\nand also figure out which page links \naren't visited yet",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "8. Mark the current URL as visited\nand also figure out which page links \naren't visited yet",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "text",
			"version": 73,
			"versionNonce": 1146717964,
			"isDeleted": false,
			"id": "zFg12okO",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 86.65217391304338,
			"y": 63.34748641304344,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 152.60792541503906,
			"height": 40,
			"seed": 1703096970,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "9. Queue unvisited \n  URLs",
			"rawText": "9. Queue unvisited \n  URLs",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "9. Queue unvisited \n  URLs",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "ellipse",
			"version": 198,
			"versionNonce": 1831813044,
			"isDeleted": false,
			"id": "FLYFR5jYBYOIaHt_fj7kG",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 300.4304709548504,
			"y": -285.3481657608696,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 33.474218089602644,
			"height": 32.459847844463226,
			"seed": 1295544266,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "e52WPzoj9WVBKRHBXk1PJ",
					"type": "arrow"
				},
				{
					"id": "hNxbwl0Gc4A12xluN6qzW",
					"type": "arrow"
				},
				{
					"id": "Lu1aUEYZ1KCa4oSMu-iRp",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 245,
			"versionNonce": 808240524,
			"isDeleted": false,
			"id": "G9IVtb--mWlhTY3R_jkfk",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 245.78260869565213,
			"y": -225.66315441593926,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 33.474218089602644,
			"height": 35.19838056680162,
			"seed": 810444310,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "e52WPzoj9WVBKRHBXk1PJ",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 262,
			"versionNonce": 1242900788,
			"isDeleted": false,
			"id": "z1xpmS2o2ZkqSurKXB4gK",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 298.5298614429049,
			"y": -225.82064874347407,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 33.474218089602644,
			"height": 32.459847844463226,
			"seed": 958902474,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "hNxbwl0Gc4A12xluN6qzW",
					"type": "arrow"
				},
				{
					"id": "oP56KnIGnoVeL3f_ev8Ad",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 235,
			"versionNonce": 1813263372,
			"isDeleted": false,
			"id": "Fj3vFq_pGSFUBXHnDSOKW",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 358.3777059061339,
			"y": -226.67752466107873,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 33.474218089602644,
			"height": 32.459847844463226,
			"seed": 294594006,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "Lu1aUEYZ1KCa4oSMu-iRp",
					"type": "arrow"
				},
				{
					"id": "4qB6rxYjlznN3Ql3WLDMz",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 282,
			"versionNonce": 897704628,
			"isDeleted": false,
			"id": "2wde9A46QkYxGmgmmTeLT",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 299.608297177211,
			"y": -137.8080136053329,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 33.474218089602644,
			"height": 32.459847844463226,
			"seed": 1403866250,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "oP56KnIGnoVeL3f_ev8Ad",
					"type": "arrow"
				},
				{
					"id": "4qB6rxYjlznN3Ql3WLDMz",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 180,
			"versionNonce": 1175048844,
			"isDeleted": false,
			"id": "e52WPzoj9WVBKRHBXk1PJ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 305.63870174501096,
			"y": -252.17131775682185,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 34.558828836015806,
			"height": 23.598329702988707,
			"seed": 1538811350,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "FLYFR5jYBYOIaHt_fj7kG",
				"focus": -0.4571490516591102,
				"gap": 4.109972057005631
			},
			"endBinding": {
				"elementId": "G9IVtb--mWlhTY3R_jkfk",
				"focus": -0.6987894451373033,
				"gap": 4.75842187894024
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
					-34.558828836015806,
					23.598329702988707
				]
			]
		},
		{
			"type": "arrow",
			"version": 155,
			"versionNonce": 1444637748,
			"isDeleted": false,
			"id": "hNxbwl0Gc4A12xluN6qzW",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 316.04072278874736,
			"y": -249.67062494042412,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.388192983322439,
			"height": 19.079083061474858,
			"seed": 1453023882,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "FLYFR5jYBYOIaHt_fj7kG",
				"focus": 0.15149339607930815,
				"gap": 3.2486752172469977
			},
			"endBinding": {
				"elementId": "z1xpmS2o2ZkqSurKXB4gK",
				"focus": 0.21991930040007562,
				"gap": 4.876729290640952
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
					1.388192983322439,
					19.079083061474858
				]
			]
		},
		{
			"type": "arrow",
			"version": 165,
			"versionNonce": 1019715852,
			"isDeleted": false,
			"id": "Lu1aUEYZ1KCa4oSMu-iRp",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 339.2661580871213,
			"y": -250.704790561333,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 27.05514703878469,
			"height": 20.244360372470798,
			"seed": 1325520854,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "FLYFR5jYBYOIaHt_fj7kG",
				"focus": 0.0916046912102059,
				"gap": 12.237776059598229
			},
			"endBinding": {
				"elementId": "Fj3vFq_pGSFUBXHnDSOKW",
				"focus": 0.6552631578947401,
				"gap": 5.549623587239697
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
					27.05514703878469,
					20.244360372470798
				]
			]
		},
		{
			"type": "arrow",
			"version": 246,
			"versionNonce": 231196084,
			"isDeleted": false,
			"id": "oP56KnIGnoVeL3f_ev8Ad",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 317.0754565953835,
			"y": -191.32803188663894,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 0.9191243301446943,
			"height": 48.07789980774297,
			"seed": 2075296522,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "zu86hR0J",
				"focus": -0.035866158848633936,
				"gap": 8.732902563016296
			},
			"endBinding": {
				"elementId": "2wde9A46QkYxGmgmmTeLT",
				"focus": -0.036044657097293265,
				"gap": 5.442905804157689
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
					-0.9191243301446943,
					48.07789980774297
				]
			]
		},
		{
			"type": "arrow",
			"version": 284,
			"versionNonce": 1741135756,
			"isDeleted": false,
			"id": "4qB6rxYjlznN3Ql3WLDMz",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 334.7097197667904,
			"y": -129.5016106116519,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 41.518233058416435,
			"height": 56.737243408327025,
			"seed": 335527370,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "h559n99i",
				"focus": -1.0879962129839031,
				"gap": 6.538475973396146
			},
			"endBinding": {
				"elementId": "nRAuFgqJ",
				"focus": 1.3984118445027458,
				"gap": 8.744939271255106
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
					34.959528604975134,
					-34.146150290918115
				],
				[
					41.518233058416435,
					-56.737243408327025
				]
			]
		},
		{
			"type": "text",
			"version": 33,
			"versionNonce": 296546100,
			"isDeleted": false,
			"id": "QagwOHkm",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 243.17391304347814,
			"y": -307.9568614130435,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 124.6558837890625,
			"height": 20,
			"seed": 1553391382,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "www.bettert.com",
			"rawText": "www.bettert.com",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "www.bettert.com",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 41,
			"versionNonce": 1598279180,
			"isDeleted": false,
			"id": "sw7MD4W9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 250.88382327055092,
			"y": -181.86638438435142,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 16.401596069335938,
			"height": 16.761133603238864,
			"seed": 796084310,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 13.408906882591092,
			"fontFamily": 1,
			"text": "s3",
			"rawText": "s3",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "s3",
			"lineHeight": 1.25,
			"baseline": 11
		},
		{
			"type": "text",
			"version": 64,
			"versionNonce": 36759732,
			"isDeleted": false,
			"id": "zu86hR0J",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 282.9486005984861,
			"y": -182.59512932362264,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 65.204345703125,
			"height": 16.761133603238868,
			"seed": 1554510998,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "oP56KnIGnoVeL3f_ev8Ad",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 13.408906882591094,
			"fontFamily": 1,
			"text": "dynamoDB",
			"rawText": "dynamoDB",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "dynamoDB",
			"lineHeight": 1.25,
			"baseline": 11
		},
		{
			"type": "text",
			"version": 99,
			"versionNonce": 607530124,
			"isDeleted": false,
			"id": "nRAuFgqJ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 384.9728920964619,
			"y": -182.59512932362264,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 44.31373596191406,
			"height": 16.761133603238864,
			"seed": 134808970,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "4qB6rxYjlznN3Ql3WLDMz",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 13.408906882591092,
			"fontFamily": 1,
			"text": "lambda",
			"rawText": "lambda",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "lambda",
			"lineHeight": 1.25,
			"baseline": 11
		},
		{
			"type": "text",
			"version": 74,
			"versionNonce": 49918516,
			"isDeleted": false,
			"id": "h559n99i",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 341.24819574018653,
			"y": -129.39674875682107,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 133.79884338378906,
			"height": 16.76113360323886,
			"seed": 1001990230,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "4qB6rxYjlznN3Ql3WLDMz",
					"type": "arrow"
				}
			],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 13.40890688259109,
			"fontFamily": 1,
			"text": "/products/daily-best",
			"rawText": "/products/daily-best",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "/products/daily-best",
			"lineHeight": 1.25,
			"baseline": 11
		},
		{
			"type": "rectangle",
			"version": 147,
			"versionNonce": 1305051788,
			"isDeleted": false,
			"id": "Ob-QjEXlMRGTp_kZ4Y_eO",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 146.53096417694758,
			"y": 374.3080794479812,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 76.36363636363637,
			"height": 78.18181818181813,
			"seed": 2070579212,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "2sUrLt0NOXmL8pXrAYNBV",
					"type": "arrow"
				},
				{
					"id": "yL-nbdvRLd0IF7ph1ggz1",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "H48gAxQc"
				}
			],
			"updated": 1712859982850,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 5,
			"versionNonce": 1694085940,
			"isDeleted": false,
			"id": "H48gAxQc",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 174.40078589880483,
			"y": 403.39898853889025,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffd8a8",
			"width": 20.623992919921875,
			"height": 20,
			"seed": 712991028,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859976715,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "S3",
			"rawText": "S3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Ob-QjEXlMRGTp_kZ4Y_eO",
			"originalText": "S3",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 171,
			"versionNonce": 384387764,
			"isDeleted": false,
			"id": "4RBlPNZaFNB5DHqlfuPA7",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -144.3781267321433,
			"y": 373.3989885388903,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 76.36363636363637,
			"height": 78.18181818181813,
			"seed": 1457521844,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "oJ_EH5Rz0a6MxkPImjLm0",
					"type": "arrow"
				},
				{
					"id": "WnOUU6hWCZl1Rc7Gks_AV",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "MD42Vpsf"
				}
			],
			"updated": 1712860012762,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 3,
			"versionNonce": 690390284,
			"isDeleted": false,
			"id": "MD42Vpsf",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -116.45230525442668,
			"y": 402.4898976297994,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 20.511993408203125,
			"height": 20,
			"seed": 506370996,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712860007418,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "ES",
			"rawText": "ES",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4RBlPNZaFNB5DHqlfuPA7",
			"originalText": "ES",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "arrow",
			"version": 40,
			"versionNonce": 1567675658,
			"isDeleted": false,
			"id": "8lgqLQdvaioi9il7dS30k",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 34.48506955456628,
			"y": 303.9285170611314,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 0,
			"height": 58.5892549302518,
			"seed": 1935434764,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165546,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "rrxxae2o_PsOckcuEc6oU",
				"gap": 10.951954561131402,
				"focus": 0.042081401262047784
			},
			"endBinding": {
				"elementId": "sc_1rJfSGJyUVyQKsUjv1",
				"gap": 5.021880985085268,
				"focus": -0.05263157894736417
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
					0,
					58.5892549302518
				]
			]
		},
		{
			"type": "arrow",
			"version": 68,
			"versionNonce": 417573642,
			"isDeleted": false,
			"id": "2sUrLt0NOXmL8pXrAYNBV",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 84.41951363764568,
			"y": 410.93089723915875,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 54.69010542432508,
			"height": 0,
			"seed": 1977908148,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165553,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "sc_1rJfSGJyUVyQKsUjv1",
				"gap": 3.3624768334920034,
				"focus": -0.05128205128205087
			},
			"endBinding": {
				"elementId": "Ob-QjEXlMRGTp_kZ4Y_eO",
				"gap": 7.421345114976816,
				"focus": 0.06313721929545696
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
					54.69010542432508,
					0
				]
			]
		},
		{
			"type": "text",
			"version": 78,
			"versionNonce": 1949101748,
			"isDeleted": false,
			"id": "SVusP9hx",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 253.24549125186672,
			"y": 382.39692919168476,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 316.20782470703125,
			"height": 40,
			"seed": 1914320180,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "6. Store images, videos, etc. in S3 and \nenable CloudFront for CDN access",
			"rawText": "6. Store images, videos, etc. in S3 and \nenable CloudFront for CDN access",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "6. Store images, videos, etc. in S3 and \nenable CloudFront for CDN access",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 29,
			"versionNonce": 1745702730,
			"isDeleted": false,
			"id": "oJ_EH5Rz0a6MxkPImjLm0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -13.01083964880739,
			"y": 409.7434272421588,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 49.99514829216255,
			"height": 1.1903606736228198,
			"seed": 1553251764,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165557,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "sc_1rJfSGJyUVyQKsUjv1",
				"gap": 5.895251591187133,
				"focus": 0.051282051282053376
			},
			"endBinding": {
				"elementId": "4RBlPNZaFNB5DHqlfuPA7",
				"gap": 5.008502427536996,
				"focus": -0.12412930070381788
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
					-49.99514829216255,
					-1.1903606736228198
				]
			]
		},
		{
			"type": "text",
			"version": 83,
			"versionNonce": 595916852,
			"isDeleted": false,
			"id": "qYGDNl1a",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -127.2074160477863,
			"y": 330.0846544379825,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 155.77590942382812,
			"height": 40,
			"seed": 239430028,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805254,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "<<Render Pages>>\n<<Scrape Content>>",
			"rawText": "<<Render Pages>>\n<<Scrape Content>>",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "<<Render Pages>>\n<<Scrape Content>>",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "rectangle",
			"version": 242,
			"versionNonce": 1146460940,
			"isDeleted": false,
			"id": "4BKFP5tsj-iSOt_vewco1",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -0.13000262131782847,
			"y": 519.2654897268653,
			"strokeColor": "#1971c2",
			"backgroundColor": "#a5d8ff",
			"width": 76.36363636363637,
			"height": 78.18181818181813,
			"seed": 14339340,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "X2XipGCU1XROyHI55v_U9",
					"type": "arrow"
				},
				{
					"id": "Oh1kGowMe7-8k9mRtaQfl",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "1tfrCAIA"
				}
			],
			"updated": 1712859934517,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 10,
			"versionNonce": 452505100,
			"isDeleted": false,
			"id": "1tfrCAIA",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 15.315823128859734,
			"y": 538.3563988177743,
			"strokeColor": "#1971c2",
			"backgroundColor": "#a5d8ff",
			"width": 45.47198486328125,
			"height": 40,
			"seed": 1148911668,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859932632,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Mongo\nDB",
			"rawText": "Mongo\nDB",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4BKFP5tsj-iSOt_vewco1",
			"originalText": "Mongo\nDB",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 42,
			"versionNonce": 1292786250,
			"isDeleted": false,
			"id": "X2XipGCU1XROyHI55v_U9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 36.867398450245744,
			"y": 460.67641586986133,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.1934135603681426,
			"height": 50.12336953545639,
			"seed": 684665140,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165559,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "sc_1rJfSGJyUVyQKsUjv1",
				"gap": 1,
				"focus": -0.025062656641611815
			},
			"endBinding": {
				"elementId": "4BKFP5tsj-iSOt_vewco1",
				"gap": 8.465704321547548,
				"focus": -0.08974435624597621
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
					-1.1934135603681426,
					50.12336953545639
				]
			]
		},
		{
			"type": "rectangle",
			"version": 247,
			"versionNonce": 1067672244,
			"isDeleted": false,
			"id": "7AA9-aJD3w7svh_8-nk0q",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -409.1168779684447,
			"y": 373.02890348356107,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 76.36363636363637,
			"height": 78.18181818181813,
			"seed": 1834612148,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "MufhPqfyl7_DgIqEVPffw",
					"type": "arrow"
				},
				{
					"id": "WnOUU6hWCZl1Rc7Gks_AV",
					"type": "arrow"
				},
				{
					"id": "NwtHsBi17iS-WC7MrBkv1",
					"type": "arrow"
				},
				{
					"id": "Oh1kGowMe7-8k9mRtaQfl",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "gjmuADZ4"
				}
			],
			"updated": 1712860036285,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 14,
			"versionNonce": 2053167028,
			"isDeleted": false,
			"id": "gjmuADZ4",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -383.4790508754937,
			"y": 402.11981257447013,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 25.087982177734375,
			"height": 20,
			"seed": 1671083020,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712860048379,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "svc",
			"rawText": "svc",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7AA9-aJD3w7svh_8-nk0q",
			"originalText": "svc",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 269,
			"versionNonce": 1351406348,
			"isDeleted": false,
			"id": "8wR85URqPaWWQ3dTfDs6g",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -409.1168779684447,
			"y": 566.8221031393218,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 76.36363636363637,
			"height": 78.18181818181813,
			"seed": 796417804,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "t_MSctg3MQq4pQ1GJyUJa",
					"type": "arrow"
				},
				{
					"id": "yL-nbdvRLd0IF7ph1ggz1",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "HBHazssv"
				}
			],
			"updated": 1712860030820,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 4,
			"versionNonce": 1593109772,
			"isDeleted": false,
			"id": "HBHazssv",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -387.4790432460992,
			"y": 595.9130122302308,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 33.08796691894531,
			"height": 20,
			"seed": 247470644,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712860032356,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "CDN",
			"rawText": "CDN",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8wR85URqPaWWQ3dTfDs6g",
			"originalText": "CDN",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "ellipse",
			"version": 84,
			"versionNonce": 1867252236,
			"isDeleted": false,
			"id": "Tp3kKDHfUSTWbGxm-Sio0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -621.7961955373353,
			"y": 458.48751065161537,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 74.90166612461917,
			"height": 72.52383545399641,
			"seed": 57069324,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "MufhPqfyl7_DgIqEVPffw",
					"type": "arrow"
				},
				{
					"id": "t_MSctg3MQq4pQ1GJyUJa",
					"type": "arrow"
				}
			],
			"updated": 1712859805255,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 39,
			"versionNonce": 2096493748,
			"isDeleted": false,
			"id": "v7mMW_A7Rrz4w_NMp1dFb",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -482.69310130589963,
			"y": 288.47261770208297,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 7.133492011868498,
			"height": 422.06494403555257,
			"seed": 521914508,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712859805255,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-7.133492011868498,
					422.06494403555257
				]
			]
		},
		{
			"type": "arrow",
			"version": 53,
			"versionNonce": 646399626,
			"isDeleted": false,
			"id": "MufhPqfyl7_DgIqEVPffw",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -546.8951697320019,
			"y": 470.3769783432881,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 130.78132720354148,
			"height": 64.20174244537492,
			"seed": 1793217548,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165562,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Tp3kKDHfUSTWbGxm-Sio0",
				"gap": 7.595539897240634,
				"focus": -0.14727883956700313
			},
			"endBinding": {
				"elementId": "7AA9-aJD3w7svh_8-nk0q",
				"gap": 6.99696456001567,
				"focus": 0.4862694302269691
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
					130.78132720354148,
					-64.20174244537492
				]
			]
		},
		{
			"type": "arrow",
			"version": 53,
			"versionNonce": 259777994,
			"isDeleted": false,
			"id": "t_MSctg3MQq4pQ1GJyUJa",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -551.6502794613755,
			"y": 514.3664785123354,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 129.59186025635802,
			"height": 77.27954969415862,
			"seed": 1915440692,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860165574,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Tp3kKDHfUSTWbGxm-Sio0",
				"gap": 1.0036059016336694,
				"focus": 0.002817314224711602
			},
			"endBinding": {
				"elementId": "8wR85URqPaWWQ3dTfDs6g",
				"gap": 12.941541236572732,
				"focus": -0.262196145876891
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
					129.59186025635802,
					77.27954969415862
				]
			]
		},
		{
			"type": "arrow",
			"version": 49,
			"versionNonce": 350979658,
			"isDeleted": false,
			"id": "WnOUU6hWCZl1Rc7Gks_AV",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -158.11921476588316,
			"y": 395.4749978801103,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 166.4481469435982,
			"height": 2.3778306706227568,
			"seed": 737115020,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860684366,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "4RBlPNZaFNB5DHqlfuPA7",
				"gap": 13.741088033739857,
				"focus": 0.410560971130061
			},
			"endBinding": {
				"elementId": "7AA9-aJD3w7svh_8-nk0q",
				"gap": 8.185879895326991,
				"focus": -0.4966409439674042
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
					-166.4481469435982,
					-2.3778306706227568
				]
			]
		},
		{
			"type": "rectangle",
			"version": 38,
			"versionNonce": 1258614324,
			"isDeleted": false,
			"id": "N_PZXx-RwNclahv07_deu",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -273.44400229109044,
			"y": 463.2431719928611,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 83.2240734717991,
			"height": 72.5238354539963,
			"seed": 926319284,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "NwtHsBi17iS-WC7MrBkv1",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "YPAus0D8"
				}
			],
			"updated": 1712860076955,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 6,
			"versionNonce": 75683468,
			"isDeleted": false,
			"id": "YPAus0D8",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -253.52795707130417,
			"y": 489.50508971985926,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 43.39198303222656,
			"height": 20,
			"seed": 505509300,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712860072945,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "cache",
			"rawText": "cache",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "N_PZXx-RwNclahv07_deu",
			"originalText": "cache",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "arrow",
			"version": 37,
			"versionNonce": 640572246,
			"isDeleted": false,
			"id": "NwtHsBi17iS-WC7MrBkv1",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -325.7562770447928,
			"y": 444.22052662787837,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 43.98986740652242,
			"height": 35.66746005934249,
			"seed": 1711798580,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860684366,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "7AA9-aJD3w7svh_8-nk0q",
				"gap": 6.996964560015556,
				"focus": -0.0646793295358809
			},
			"endBinding": {
				"elementId": "N_PZXx-RwNclahv07_deu",
				"gap": 8.322407347179933,
				"focus": -0.2981409226532014
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
					43.98986740652242,
					35.66746005934249
				]
			]
		},
		{
			"type": "arrow",
			"version": 89,
			"versionNonce": 1593322762,
			"isDeleted": false,
			"id": "Oh1kGowMe7-8k9mRtaQfl",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -13.071543857890447,
			"y": 564.3009754943314,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 343.5965319049991,
			"height": 103.43563417209316,
			"seed": 1665998476,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860684366,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "4BKFP5tsj-iSOt_vewco1",
				"gap": 12.941541236572618,
				"focus": -0.21679797038032295
			},
			"endBinding": {
				"elementId": "7AA9-aJD3w7svh_8-nk0q",
				"gap": 9.65461965685904,
				"focus": 0.16488357741424203
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
					-301.98449516909955,
					-17.833730029671187
				],
				[
					-343.5965319049991,
					-103.43563417209316
				]
			]
		},
		{
			"type": "arrow",
			"version": 143,
			"versionNonce": 1303675030,
			"isDeleted": false,
			"id": "yL-nbdvRLd0IF7ph1ggz1",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -326.9451923801041,
			"y": 630.8802342717706,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 576.6239376260366,
			"height": 212.81584502074332,
			"seed": 68520628,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712860684367,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "8wR85URqPaWWQ3dTfDs6g",
				"gap": 5.808049224704234,
				"focus": 0.6438147272678548
			},
			"endBinding": {
				"elementId": "Ob-QjEXlMRGTp_kZ4Y_eO",
				"gap": 10.139330010988715,
				"focus": -1.160154310131015
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
					576.6239376260366,
					-5.9445766765570625
				],
				[
					559.9791229316768,
					-212.81584502074332
				]
			]
		},
		{
			"type": "text",
			"version": 56,
			"versionNonce": 94536756,
			"isDeleted": false,
			"id": "kWloL9bw",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -159.3081301011946,
			"y": 471.56557934004104,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 223.11984252929688,
			"height": 40,
			"seed": 121235980,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805255,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "6. Index product by search \nterms in Elastic Search",
			"rawText": "6. Index product by search \nterms in Elastic Search",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "6. Index product by search \nterms in Elastic Search",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "text",
			"version": 101,
			"versionNonce": 2128480524,
			"isDeleted": false,
			"id": "2J6r7nmn",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 97.49758232607132,
			"y": 525.0667694290547,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 300.0478515625,
			"height": 60,
			"seed": 717236108,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805255,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "7. Scrape and structure the content \ninto MongoDB document storage. \nRefer to CDN urls from S3",
			"rawText": "7. Scrape and structure the content \ninto MongoDB document storage. \nRefer to CDN urls from S3",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "7. Scrape and structure the content \ninto MongoDB document storage. \nRefer to CDN urls from S3",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "text",
			"version": 21,
			"versionNonce": 1823202740,
			"isDeleted": false,
			"id": "Tk3yhDjJ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -589.6954814839271,
			"y": 406.1752358979131,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 115.42391967773438,
			"height": 20,
			"seed": 1770680716,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859805255,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "1. Access Page",
			"rawText": "1. Access Page",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1. Access Page",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 14,
			"versionNonce": 939105332,
			"isDeleted": false,
			"id": "flHLBf0N",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -598.017888831107,
			"y": 607.1019275655424,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 117.55191040039062,
			"height": 20,
			"seed": 216020492,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859812372,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "2. Access CDN",
			"rawText": "2. Access CDN",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "2. Access CDN",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 44,
			"versionNonce": 824090676,
			"isDeleted": false,
			"id": "AkueTOBc",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -303.16688567387587,
			"y": 434.7092039453871,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 120.22392272949219,
			"height": 20,
			"seed": 900457780,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859874119,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "2. Check Cache",
			"rawText": "2. Check Cache",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "2. Check Cache",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 42,
			"versionNonce": 1199511436,
			"isDeleted": false,
			"id": "fQKmaopa",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -293.6555629913845,
			"y": 350.2962151382766,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 150.14390563964844,
			"height": 40,
			"seed": 2023816500,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859902514,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "3. Search product \nby search term",
			"rawText": "3. Search product \nby search term",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "3. Search product \nby search term",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "text",
			"version": 47,
			"versionNonce": 57403444,
			"isDeleted": false,
			"id": "KVpFzqUU",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -284.14424030889325,
			"y": 575.0012135121342,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 225.15185546875,
			"height": 40,
			"seed": 94382988,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712859897669,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "4. Get product details and \nURLs cache results",
			"rawText": "4. Get product details and \nURLs cache results",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "4. Get product details and \nURLs cache results",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "diamond",
			"version": 88,
			"versionNonce": 886267572,
			"isDeleted": false,
			"id": "sc_1rJfSGJyUVyQKsUjv1",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -8.315882516644933,
			"y": 366.94102983263633,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#e9ecef",
			"width": 90.35756548366771,
			"height": 92.73539615429047,
			"seed": 119270924,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "8lgqLQdvaioi9il7dS30k",
					"type": "arrow"
				},
				{
					"id": "2sUrLt0NOXmL8pXrAYNBV",
					"type": "arrow"
				},
				{
					"id": "oJ_EH5Rz0a6MxkPImjLm0",
					"type": "arrow"
				},
				{
					"id": "X2XipGCU1XROyHI55v_U9",
					"type": "arrow"
				}
			],
			"updated": 1712860143885,
			"link": null,
			"locked": false
		},
		{
			"id": "7-kviq0H5gNMqZ-_4ySa2",
			"type": "arrow",
			"x": 35.6739848898776,
			"y": -219.86299535200425,
			"width": 0,
			"height": 27.345052712162556,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#e9ecef",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 149156490,
			"version": 17,
			"versionNonce": 838636630,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1712860696737,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					27.345052712162556
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "dufUYwEVuJAv311LKc0Jn",
				"focus": -0.024070888924200062,
				"gap": 6.1669927700495
			},
			"endBinding": {
				"elementId": "3bWb5CvScXNg9wgERwlUE",
				"focus": -0.00905597528117773,
				"gap": 3.494505139841692
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1e1e1e",
		"currentItemBackgroundColor": "#e9ecef",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 1,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 16,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 1064.072700273182,
		"scrollY": 430.2452792957821,
		"zoom": {
			"value": 0.8411027852862772
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