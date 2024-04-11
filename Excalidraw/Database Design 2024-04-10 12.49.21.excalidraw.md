---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Customer Table

customerID (PK)
CustomerName
CustomerEmail
CustomerAddress
 ^7wJ5aaOa

Product Table

ProductID (PK)
ProductName
Description
Price
 ^7QYYhzPh

Order Table

OrderID (PK)
CustomerID
OrderDate
 ^vK4mdjgK

OrderDetails Table

OrderDetailID (PK)
OrderID (FK)
ProductID (FK)
Quantity
TotalPrice
 ^JUIF193x

Supplier Table

SupplierID (PK)
SupplierName
SupplierEmail
SupplierPhone
 ^r6LpuQxZ

ProductSupplier Table

ProductID (PK)
SupplierID (FK)
 ^JYvKKjY9

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
			"version": 150,
			"versionNonce": 1122545413,
			"isDeleted": false,
			"id": "UIc_FTNZKrwSYFPrbejKd",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -318,
			"y": -234.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 161,
			"height": 151,
			"seed": 1982139115,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1712778955209,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 119,
			"versionNonce": 1082224587,
			"isDeleted": false,
			"id": "7wJ5aaOa",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -302,
			"y": -219.5234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 133.45587158203125,
			"height": 140,
			"seed": 1324928907,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712778955209,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Customer Table\n\ncustomerID (PK)\nCustomerName\nCustomerEmail\nCustomerAddress\n",
			"rawText": "Customer Table\n\ncustomerID (PK)\nCustomerName\nCustomerEmail\nCustomerAddress\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Customer Table\n\ncustomerID (PK)\nCustomerName\nCustomerEmail\nCustomerAddress\n",
			"lineHeight": 1.25,
			"baseline": 134
		},
		{
			"type": "rectangle",
			"version": 189,
			"versionNonce": 375817829,
			"isDeleted": false,
			"id": "wC-VCdBQ9703ipuhLT8aW",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -97.5,
			"y": -235.5234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 161,
			"height": 151,
			"seed": 1079340747,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1712778955210,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 194,
			"versionNonce": 1308049003,
			"isDeleted": false,
			"id": "7QYYhzPh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -80.5,
			"y": -222.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 123.21591186523438,
			"height": 140,
			"seed": 1358126443,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712778955210,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Product Table\n\nProductID (PK)\nProductName\nDescription\nPrice\n",
			"rawText": "Product Table\n\nProductID (PK)\nProductName\nDescription\nPrice\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Product Table\n\nProductID (PK)\nProductName\nDescription\nPrice\n",
			"lineHeight": 1.25,
			"baseline": 134
		},
		{
			"type": "rectangle",
			"version": 300,
			"versionNonce": 1194140101,
			"isDeleted": false,
			"id": "RASXca5CZniIT7fXnCCcv",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 127.5,
			"y": -233.5234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 161,
			"height": 151,
			"seed": 429725605,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1712778960028,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 423,
			"versionNonce": 1729012005,
			"isDeleted": false,
			"id": "vK4mdjgK",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 143.5,
			"y": -219.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 104.86392211914062,
			"height": 120,
			"seed": 935648005,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712778960028,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Order Table\n\nOrderID (PK)\nCustomerID\nOrderDate\n",
			"rawText": "Order Table\n\nOrderID (PK)\nCustomerID\nOrderDate\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Order Table\n\nOrderID (PK)\nCustomerID\nOrderDate\n",
			"lineHeight": 1.25,
			"baseline": 114
		},
		{
			"type": "rectangle",
			"version": 399,
			"versionNonce": 2006717579,
			"isDeleted": false,
			"id": "b4faZ1uwsXj5wP8VPpllw",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -316.5,
			"y": -57.5234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 186,
			"height": 168,
			"seed": 1717120165,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1712778968647,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 475,
			"versionNonce": 1004489515,
			"isDeleted": false,
			"id": "JUIF193x",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -300.5,
			"y": -43.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 153.5198974609375,
			"height": 160,
			"seed": 506875909,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712778968647,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "OrderDetails Table\n\nOrderDetailID (PK)\nOrderID (FK)\nProductID (FK)\nQuantity\nTotalPrice\n",
			"rawText": "OrderDetails Table\n\nOrderDetailID (PK)\nOrderID (FK)\nProductID (FK)\nQuantity\nTotalPrice\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "OrderDetails Table\n\nOrderDetailID (PK)\nOrderID (FK)\nProductID (FK)\nQuantity\nTotalPrice\n",
			"lineHeight": 1.25,
			"baseline": 154
		},
		{
			"type": "rectangle",
			"version": 346,
			"versionNonce": 511441989,
			"isDeleted": false,
			"id": "2J6IelmXySmosBHi5ohcn",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -91.5,
			"y": -53.5234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 161,
			"height": 151,
			"seed": 675022949,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1712778973100,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 440,
			"versionNonce": 1419652005,
			"isDeleted": false,
			"id": "r6LpuQxZ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -75.5,
			"y": -39.0234375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 119.56790161132812,
			"height": 140,
			"seed": 516404165,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712778973100,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Supplier Table\n\nSupplierID (PK)\nSupplierName\nSupplierEmail\nSupplierPhone\n",
			"rawText": "Supplier Table\n\nSupplierID (PK)\nSupplierName\nSupplierEmail\nSupplierPhone\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Supplier Table\n\nSupplierID (PK)\nSupplierName\nSupplierEmail\nSupplierPhone\n",
			"lineHeight": 1.25,
			"baseline": 134
		},
		{
			"type": "rectangle",
			"version": 417,
			"versionNonce": 428044037,
			"isDeleted": false,
			"id": "_M1-krBsJzmvp5zM5rkdI",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 124.5,
			"y": -54.2734375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 208,
			"height": 151,
			"seed": 1466087051,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1712778973100,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 517,
			"versionNonce": 686462554,
			"isDeleted": false,
			"id": "JYvKKjY9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 140.5,
			"y": -40.51417824074076,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 172.1438751220703,
			"height": 100,
			"seed": 1853992235,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712779041777,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "ProductSupplier Table\n\nProductID (PK)\nSupplierID (FK)\n",
			"rawText": "ProductSupplier Table\n\nProductID (PK)\nSupplierID (FK)\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "ProductSupplier Table\n\nProductID (PK)\nSupplierID (FK)\n",
			"lineHeight": 1.25,
			"baseline": 94
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1e1e1e",
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
		"currentItemEndArrowhead": "arrow",
		"scrollX": 339.41666666666663,
		"scrollY": 412.42737268518516,
		"zoom": {
			"value": 1.35
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