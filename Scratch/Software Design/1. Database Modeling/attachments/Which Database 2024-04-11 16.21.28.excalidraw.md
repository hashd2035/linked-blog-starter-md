---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
ChatRoom
 ^aF2b61o7

Message ^784kcENm

ChatRoom
History ^twqRsJXW

Members ^nlhagth6

Member ContactInfo ^6iFJrlGx

has messages 
1 to *
 ^iGH0DjTU

a member has many chatrooms
* to 1..2 ^xEnEeB0A

A chatroomHistory has many chatRoom ^gfC8oYvE

* ^mCQzqpoA

1 ^Lzp4CLA9

1 ^6NSIiBtp

1 ^gVYw3UNK

1  ^2iYJhgRP

* ^w6AtIk32

[How to specify follower like relations in ERD](https://stackoverflow.com/questions/57752785/how-to-specify-this-form-of-follower-like-data-in-a-data-model-erd-or-database) ^rtQ10vlS

CREATE TABLE public.user (
    id bigint NOT NULL,
    name character varying(100) NOT NULL
); 

CREATE TABLE public.follower(
    id bigint NOT NULL,
    follower_id bigint NOT NULL
);

-- pk user
ALTER TABLE ONLY public.user
    ADD CONSTRAINT user_pkey PRIMARY KEY (id);

-- pk follower
ALTER TABLE ONLY public.follower
    ADD CONSTRAINT follower_pkey PRIMARY KEY (id, follower_id);

-- foreign keys

ALTER TABLE ONLY public.follower
    ADD CONSTRAINT follower_fk1 FOREIGN KEY (id) REFERENCES public.user(id);

ALTER TABLE ONLY public.follower
    ADD CONSTRAINT follower_fk2 FOREIGN KEY (follower_id) REFERENCES public.user(id); ^7INNDr7C

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.25",
	"elements": [
		{
			"type": "rectangle",
			"version": 40,
			"versionNonce": 472294597,
			"isDeleted": false,
			"id": "YDFarUrbsWiYOWoXc6Ix-",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -307,
			"y": -222.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 170,
			"height": 154,
			"seed": 752200357,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "aF2b61o7"
				},
				{
					"id": "MlrIL2PgtZdVh8O4hqnnp",
					"type": "arrow"
				},
				{
					"id": "sNt6KXxU1ViHYDfIqBRYc",
					"type": "arrow"
				},
				{
					"id": "lkA0ZP3yeTofULhoEMTfh",
					"type": "arrow"
				}
			],
			"updated": 1712878165042,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 11,
			"versionNonce": 1210702891,
			"isDeleted": false,
			"id": "aF2b61o7",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -269.8899612426758,
			"y": -170.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 95.77992248535156,
			"height": 50,
			"seed": 461180805,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712877701353,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "ChatRoom\n",
			"rawText": "ChatRoom\n",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YDFarUrbsWiYOWoXc6Ix-",
			"originalText": "ChatRoom\n",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "rectangle",
			"version": 98,
			"versionNonce": 388239435,
			"isDeleted": false,
			"id": "Ctsmw7ihTetqWOor6cGjX",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 24,
			"y": -218.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 149,
			"seed": 268111211,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "784kcENm"
				},
				{
					"id": "MlrIL2PgtZdVh8O4hqnnp",
					"type": "arrow"
				},
				{
					"id": "sNt6KXxU1ViHYDfIqBRYc",
					"type": "arrow"
				}
			],
			"updated": 1712877818846,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 58,
			"versionNonce": 1536968869,
			"isDeleted": false,
			"id": "784kcENm",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 61.36003875732422,
			"y": -156.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 82.27992248535156,
			"height": 25,
			"seed": 489962027,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712877719216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Message",
			"rawText": "Message",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Ctsmw7ihTetqWOor6cGjX",
			"originalText": "Message",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 147,
			"versionNonce": 316828261,
			"isDeleted": false,
			"id": "AQTB8QlfFVwhiFjrR3KoG",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -307.5,
			"y": 5.4765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 149,
			"seed": 1858990443,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "twqRsJXW"
				},
				{
					"id": "lkA0ZP3yeTofULhoEMTfh",
					"type": "arrow"
				}
			],
			"updated": 1712878232528,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 121,
			"versionNonce": 351623339,
			"isDeleted": false,
			"id": "twqRsJXW",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -276.8899612426758,
			"y": 54.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 95.77992248535156,
			"height": 50,
			"seed": 780307467,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712877735880,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "ChatRoom\nHistory",
			"rawText": "ChatRoom\nHistory",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AQTB8QlfFVwhiFjrR3KoG",
			"originalText": "ChatRoom\nHistory",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "rectangle",
			"version": 205,
			"versionNonce": 1783748037,
			"isDeleted": false,
			"id": "oKDt41Ou0cIz8_TkvWUPL",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 21.5,
			"y": 4.4765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 149,
			"seed": 85765541,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "nlhagth6"
				},
				{
					"id": "sNt6KXxU1ViHYDfIqBRYc",
					"type": "arrow"
				},
				{
					"id": "4l2VixdYNlXzU1PjCIcmG",
					"type": "arrow"
				},
				{
					"id": "d3k8qr-DZN8UxOHh5ywof",
					"type": "arrow"
				}
			],
			"updated": 1712878232529,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 193,
			"versionNonce": 1573070603,
			"isDeleted": false,
			"id": "nlhagth6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 60.260040283203125,
			"y": 66.4765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 79.47991943359375,
			"height": 25,
			"seed": 2061611269,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712877746677,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Members",
			"rawText": "Members",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "oKDt41Ou0cIz8_TkvWUPL",
			"originalText": "Members",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 261,
			"versionNonce": 1963278891,
			"isDeleted": false,
			"id": "FHR84qtTA9Snb9phrHpjE",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 27.5,
			"y": 227.4765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 149,
			"seed": 1325765931,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "6iFJrlGx"
				},
				{
					"id": "d3k8qr-DZN8UxOHh5ywof",
					"type": "arrow"
				}
			],
			"updated": 1712877827205,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 274,
			"versionNonce": 1635903909,
			"isDeleted": false,
			"id": "6iFJrlGx",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 45.840049743652344,
			"y": 276.9765625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 120.31990051269531,
			"height": 50,
			"seed": 932165579,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712877792012,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Member\nContactInfo",
			"rawText": "Member ContactInfo",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FHR84qtTA9Snb9phrHpjE",
			"originalText": "Member ContactInfo",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "arrow",
			"version": 31,
			"versionNonce": 1209342853,
			"isDeleted": false,
			"id": "MlrIL2PgtZdVh8O4hqnnp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -129,
			"y": -151.2890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 138,
			"height": 1,
			"seed": 1445713323,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712878930924,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "YDFarUrbsWiYOWoXc6Ix-",
				"gap": 8,
				"focus": -0.07204334329194287
			},
			"endBinding": {
				"elementId": "Ctsmw7ihTetqWOor6cGjX",
				"gap": 15,
				"focus": 0.1257933539263478
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					138,
					-1
				]
			]
		},
		{
			"type": "arrow",
			"version": 113,
			"versionNonce": 323793157,
			"isDeleted": false,
			"id": "sNt6KXxU1ViHYDfIqBRYc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -119.00000000000001,
			"y": -75.2890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 220,
			"height": 73,
			"seed": 1062139621,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712878930938,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "YDFarUrbsWiYOWoXc6Ix-",
				"gap": 18,
				"focus": 0.3379806653704904
			},
			"endBinding": {
				"elementId": "oKDt41Ou0cIz8_TkvWUPL",
				"gap": 6.765625,
				"focus": 0.8115294636197193
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					220,
					73
				]
			]
		},
		{
			"type": "arrow",
			"version": 201,
			"versionNonce": 62780357,
			"isDeleted": false,
			"id": "4l2VixdYNlXzU1PjCIcmG",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 192.89271112451038,
			"y": 122.4981920424623,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 150.5316151507603,
			"height": 120.09830952568734,
			"seed": 1131761707,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712878930940,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "oKDt41Ou0cIz8_TkvWUPL",
				"gap": 14.392711124510356,
				"focus": 0.6818577101001743
			},
			"endBinding": {
				"elementId": "oKDt41Ou0cIz8_TkvWUPL",
				"gap": 17.504088513712304,
				"focus": -1.1047493652699558
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					150.5316151507603,
					-27.825011674139517
				],
				[
					2.987752475265893,
					-120.09830952568734
				]
			]
		},
		{
			"type": "arrow",
			"version": 45,
			"versionNonce": 749168965,
			"isDeleted": false,
			"id": "d3k8qr-DZN8UxOHh5ywof",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 97,
			"y": 165.7109375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 2,
			"height": 55,
			"seed": 2116300709,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712878930953,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "oKDt41Ou0cIz8_TkvWUPL",
				"gap": 12.234375,
				"focus": 0.07577941341094817
			},
			"endBinding": {
				"elementId": "FHR84qtTA9Snb9phrHpjE",
				"gap": 6.765625,
				"focus": -0.04980829508563752
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					2,
					55
				]
			]
		},
		{
			"type": "text",
			"version": 99,
			"versionNonce": 268728261,
			"isDeleted": false,
			"id": "iGH0DjTU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -122,
			"y": -173.7890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 115.64791870117188,
			"height": 60,
			"seed": 21051589,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878148459,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "has messages \n1 to *\n",
			"rawText": "has messages \n1 to *\n",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "has messages \n1 to *\n",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "text",
			"version": 208,
			"versionNonce": 2136118443,
			"isDeleted": false,
			"id": "xEnEeB0A",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -154.77593231201172,
			"y": -63.2890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 237.55186462402344,
			"height": 40,
			"seed": 1630933099,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878140753,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "a member has many chatrooms\n* to 1..2",
			"rawText": "a member has many chatrooms\n* to 1..2",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "a member has many chatrooms\n* to 1..2",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 57,
			"versionNonce": 877510213,
			"isDeleted": false,
			"id": "lkA0ZP3yeTofULhoEMTfh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -232.00000000000003,
			"y": 2.7109375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 3.9848214285714505,
			"height": 69.734375,
			"seed": 2024574027,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712878930929,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "AQTB8QlfFVwhiFjrR3KoG",
				"gap": 2.765625,
				"focus": -0.08960167443466253
			},
			"endBinding": {
				"elementId": "YDFarUrbsWiYOWoXc6Ix-",
				"gap": 1,
				"focus": 0.01742769255353148
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					3.9848214285714505,
					-69.734375
				]
			]
		},
		{
			"type": "text",
			"version": 108,
			"versionNonce": 1168664555,
			"isDeleted": false,
			"id": "gfC8oYvE",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -439.7839050292969,
			"y": -38.2890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 303.56781005859375,
			"height": 20,
			"seed": 973716651,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878222295,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "A chatroomHistory has many chatRoom",
			"rawText": "A chatroomHistory has many chatRoom",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "A chatroomHistory has many chatRoom",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 14,
			"versionNonce": 700849803,
			"isDeleted": false,
			"id": "mCQzqpoA",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -248.12799835205078,
			"y": -62.2890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 8.255996704101562,
			"height": 20,
			"seed": 1008277355,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878215947,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "*",
			"rawText": "*",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "*",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 13,
			"versionNonce": 152335397,
			"isDeleted": false,
			"id": "Lzp4CLA9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -247.16799926757812,
			"y": -15.2890625,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 4.33599853515625,
			"height": 20,
			"seed": 1227238219,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878219216,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "1",
			"rawText": "1",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 2,
			"versionNonce": 1655998629,
			"isDeleted": false,
			"id": "6NSIiBtp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 71.83200073242188,
			"y": 175.7109375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 4.33599853515625,
			"height": 20,
			"seed": 2088369899,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878268856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "1",
			"rawText": "1",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 2,
			"versionNonce": 89435845,
			"isDeleted": false,
			"id": "gVYw3UNK",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 117.83200073242188,
			"y": 206.7109375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 4.33599853515625,
			"height": 20,
			"seed": 688276171,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878272197,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "1",
			"rawText": "1",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 3,
			"versionNonce": 1774348517,
			"isDeleted": false,
			"id": "2iYJhgRP",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 268.7583712645485,
			"y": 37.183824655327044,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 12.33599853515625,
			"height": 20,
			"seed": 425126923,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878401092,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "1 ",
			"rawText": "1 ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1 ",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 2,
			"versionNonce": 1574139653,
			"isDeleted": false,
			"id": "w6AtIk32",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 258.5665943688001,
			"y": 136.2612249266602,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 8.255996704101562,
			"height": 20,
			"seed": 727125643,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878406379,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "*",
			"rawText": "*",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "*",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 114,
			"versionNonce": 825179147,
			"isDeleted": false,
			"id": "rtQ10vlS",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -229.1348207032579,
			"y": -273.50333175107556,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 403.87255859375,
			"height": 20,
			"seed": 63650245,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878493570,
			"link": "https://stackoverflow.com/questions/57752785/how-to-specify-this-form-of-follower-like-data-in-a-data-model-erd-or-database",
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "🌐[[How to specify follower like relations in ERD]]",
			"rawText": "[How to specify follower like relations in ERD](https://stackoverflow.com/questions/57752785/how-to-specify-this-form-of-follower-like-data-in-a-data-model-erd-or-database)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "🌐[[How to specify follower like relations in ERD]]",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 113,
			"versionNonce": 1436570219,
			"isDeleted": false,
			"id": "7INNDr7C",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 375.64925747510296,
			"y": -295.52053181137177,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 742.8474731445312,
			"height": 500,
			"seed": 747069067,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712878768214,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "CREATE TABLE public.user (\n    id bigint NOT NULL,\n    name character varying(100) NOT NULL\n); \n\nCREATE TABLE public.follower(\n    id bigint NOT NULL,\n    follower_id bigint NOT NULL\n);\n\n-- pk user\nALTER TABLE ONLY public.user\n    ADD CONSTRAINT user_pkey PRIMARY KEY (id);\n\n-- pk follower\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_pkey PRIMARY KEY (id, follower_id);\n\n-- foreign keys\n\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_fk1 FOREIGN KEY (id) REFERENCES public.user(id);\n\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_fk2 FOREIGN KEY (follower_id) REFERENCES public.user(id);",
			"rawText": "CREATE TABLE public.user (\n    id bigint NOT NULL,\n    name character varying(100) NOT NULL\n); \n\nCREATE TABLE public.follower(\n    id bigint NOT NULL,\n    follower_id bigint NOT NULL\n);\n\n-- pk user\nALTER TABLE ONLY public.user\n    ADD CONSTRAINT user_pkey PRIMARY KEY (id);\n\n-- pk follower\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_pkey PRIMARY KEY (id, follower_id);\n\n-- foreign keys\n\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_fk1 FOREIGN KEY (id) REFERENCES public.user(id);\n\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_fk2 FOREIGN KEY (follower_id) REFERENCES public.user(id);",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CREATE TABLE public.user (\n    id bigint NOT NULL,\n    name character varying(100) NOT NULL\n); \n\nCREATE TABLE public.follower(\n    id bigint NOT NULL,\n    follower_id bigint NOT NULL\n);\n\n-- pk user\nALTER TABLE ONLY public.user\n    ADD CONSTRAINT user_pkey PRIMARY KEY (id);\n\n-- pk follower\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_pkey PRIMARY KEY (id, follower_id);\n\n-- foreign keys\n\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_fk1 FOREIGN KEY (id) REFERENCES public.user(id);\n\nALTER TABLE ONLY public.follower\n    ADD CONSTRAINT follower_fk2 FOREIGN KEY (follower_id) REFERENCES public.user(id);",
			"lineHeight": 1.25,
			"baseline": 494
		},
		{
			"type": "text",
			"version": 61,
			"versionNonce": 1369701925,
			"isDeleted": true,
			"id": "lPsZFdvp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 325.07665955835716,
			"y": 226.77638073010036,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 8,
			"height": 20,
			"seed": 242661445,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712879016661,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "",
			"rawText": "",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25,
			"baseline": 14
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
		"currentItemFontSize": 16,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": null,
		"scrollX": 698.7231432454186,
		"scrollY": 455.37457808248104,
		"zoom": {
			"value": 0.8175426462359086
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