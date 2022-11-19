<!-- Samples to categories -->

<h1 style="text-align:center;">Samples crud</h1>

## Mockup For Response: 

```json
{
  "data":"data of response",
  "message":"success or fail",
  "code":"status of response code",
  "error":{"key":"if thier any errors in response"},
}
```
## Mockup For Response Auth:
```json
{
  "data":"data of response",
  "token": "data of token",
  "message":"success or fail",
  "code":"status of response code",
  "error":{"key":"if thier any errors in response"},
}
```

___
## Categories:

### Index

<table>
<tr>
<th style="text-align:start">use</th>
<td>get all categories</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>No need</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/categories</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "data": [
            {
                "id": 2,
                "name": "category 2",
                "description": "category 2",
                "image":null,
                "created_at": "2022-10-10T10:10:18.000000Z",
                "updated_at": "2022-10-18T12:03:23.000000Z"
            }
        ]
    },
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Store

<table>
<tr>
<th style="text-align:start">use</th>
<td>add new category</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>name-description-image</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/categories</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 60,
        "name": "category 50",
        "description": null,
        "image": null,
        "created_at": "2022-11-01T12:43:54.000000Z",
        "updated_at": "2022-11-01T12:43:54.000000Z"
    },
    "message": "success",
    "code": 201,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "name": [
            "The name field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>


___

### Update

<table>
<tr>
<th style="text-align:start">use</th>
<td>update category that is selected</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>cateid-name-description-image</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/categories/{category}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 2,
        "name": "category",
        "description": "category 2",
        "image"      : null,
        "created_at": "2022-10-10T10:10:18.000000Z",
        "updated_at": "2022-11-01T12:46:51.000000Z"
    },
    "message": "success",
    "code": 202,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "name": [
            "The name field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>

___

### Destroy

<table>
<tr>
<th style="text-align:start">use</th>
<td>delete category that is selected</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>cateid</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>DELETE</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/categories/{category}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 31,
        "name": "h",
        "description": "1",
        "image":null,
        "created_at": "2022-10-31T18:00:06.000000Z",
        "updated_at": "2022-10-31T18:00:06.000000Z"
    },
    "message": "deleted",
    "code": 204,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
{
    "data": "",
    "message": "fail",
    "code": 204,
    "errors": "not found this category id"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Show

<table>
<tr>
<th style="text-align:start">use</th>
<td>show category that is selected</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>cateid</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/categories/{category}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "data": [
            {
                "id": 1,
                "name": "product 1",
                "description": "product 1",
                "price": 6000,
                "offer": 1000,
                "image": "images/product//202211021755about.webp",
                "available": "yes",
                "category_id": 1,
                "created_at": "2022-11-02T16:45:51.000000Z",
                "updated_at": "2022-11-02T17:55:25.000000Z"
            }
        ]
    },
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>


___
## Products:

### Index

<table>
<tr>
<th style="text-align:start">use</th>
<td>get all products</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>no need</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/products</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "data": [
            {
                "id": 111,
                "name": "product 1",
                "description": "product",
                "price": 6000,
                "offer": 3000,
                "image": "images/product//202210181231back-2_1627326624.webp",
                "available": "yes",
                "category_id": 2,
                "created_at": "2022-10-18T12:31:13.000000Z",
                "updated_at": "2022-10-18T12:31:13.000000Z"
            }
        ]
    },
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Store

<table>
<tr>
<th style="text-align:start">use</th>
<td>add new product</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>id-name-description-price-offer-image-quantity-available-category_id</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/products</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 322,
        "name": "product 5555",
        "description": "product 5555",
        "price": "555",
        "offer": "100",
        "image": {},
        "available": "yes",
        "category_id": "18",
        "created_at": "2022-11-01T13:08:16.000000Z",
        "updated_at": "2022-11-01T13:08:16.000000Z"
    },
    "message": "success",
    "code": 201,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "name": [
            "The name field is required."
        ],
        "description": [
            "The description field is required."
        ],
        "image": [
            "The image field is required."
        ],
        "price": [
            "The price field is required."
        ],
        "offer": [
            "The offer field is required."
        ],
        "available": [
            "The available field is required."
        ],
        "category_id": [
            "The category id field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>


___

### Update

<table>
<tr>
<th style="text-align:start">use</th>
<td>update product that is selected</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>prodid-id-name-description-price-offer-image-quantity-available-category_id</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/products/{product}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 319,
        "name": "product 9999",
        "description": "product 9999",
        "price": "888",
        "offer": "100",
        "image": "images/product//202211011151back-2_1627326624.webp",
        "available": "yes",
        "category_id": "8",
        "created_at": "2022-11-01T11:51:23.000000Z",
        "updated_at": "2022-11-01T13:10:11.000000Z"
    },
    "message": "success",
    "code": 202,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}


{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "name": [
            "The name field is required."
        ],
        "description": [
            "The description field is required."
        ],
        "price": [
            "The price field is required."
        ],
        "offer": [
            "The offer field is required."
        ],
        "available": [
            "The available field is required."
        ],
        "category_id": [
            "The category id field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>

___

### Destroy

<table>
<tr>
<th style="text-align:start">use</th>
<td>delete product that is selected</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>No need</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>delete</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/products/{product}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 321,
        "name": "product 5555",
        "description": "product 5555",
        "price": 555,
        "offer": 100,
        "image": "images/product//202211011308back-2_1627326624.webp",
        "available": "yes",
        "category_id": 18,
        "created_at": "2022-11-01T13:08:16.000000Z",
        "updated_at": "2022-11-01T13:08:16.000000Z"
    },
    "message": "deleted",
    "code": 204,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
{
    "data": "",
    "message": "fail",
    "code": 204,
    "errors": "not found this product id"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Show

<table>
<tr>
<th style="text-align:start">use</th>
<td>show product that is selected</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>prodid</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/products/{product}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 319,
        "name": "product 9999",
        "description": "product 9999",
        "price": 888,
        "offer": 100,
        "image": "images/product//202211011151back-2_1627326624.webp",
        "available": "yes",
        "category_id": 8,
        "created_at": "2022-11-01T11:51:23.000000Z",
        "updated_at": "2022-11-01T13:10:11.000000Z"
    },
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>


___
## Actions:

### Search about product by name

<table>
<tr>
<th style="text-align:start">use</th>
<td>get product by name</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>name</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/searchproductnames</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "data": [
            {
                "id": 117,
                "name": "product 4",
                "description": "product",
                "price": 6000,
                "offer": 3000,
                "image": "images/product//202210181231back-2_1627326624.webp",
                "available": "yes",
                "category_id": 2,
                "created_at": "2022-10-18T12:31:37.000000Z",
                "updated_at": "2022-10-18T12:31:37.000000Z"
            }
        ]
    },
    "message": "success",
    "code": 200,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
{
    "data": {
        "data": []
    },
    "message": "success",
    "code": 200,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<td> format not found data </td>
<td>
<pre>
{
    "data": [],
    "message": "not found data",
    "code": 404,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "name": [
            "The name must be at least 3 characters."
        ]
    }
}
</pre>
</td>
</tr>
</table>

___

### View products according to category

<table>
<tr>
<th style="text-align:start">use</th>
<td>get product by category</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>cateid</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/productsaccordingcategory/{cate_id}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "data": [
             {
                "id": 131,
                "name": "product 1",
                "description": "product",
                "price": 6000,
                "offer": 3000,
                "image": "images/product//202210181233back-2_1627326624.webp",
                "available": "yes",
                "category_id": 4,
                "created_at": "2022-10-18T12:33:55.000000Z",
                "updated_at": "2022-10-18T12:33:55.000000Z"
            }
        ]
    },
    "message": "success",
    "code": 200,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
{
    "data": {
        "data": []
    },
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<td>format not found data</td>
<td>
<pre>
{
    "data": [],
    "message": "not found data",
    "code": 404,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Filter products

<table>
<tr>
<th style="text-align:start">use</th>
<td>get product by name and min price and max price and category</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>category_id-name-min_price-max_price</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>api/filterproducts</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "data": [
            {
                "id": 137,
                "name": "product 4",
                "description": "product",
                "price": 6000,
                "offer": 3000,
                "image": "images/product//202210181234back-2_1627326624.webp",
                "available": "yes",
                "category_id": 4,
                "created_at": "2022-10-18T12:34:08.000000Z",
                "updated_at": "2022-10-18T12:34:08.000000Z"
            }
        ]
    },
    "message": "success",
    "code": 200,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Format response Not found data</th>
<td>
<pre>
{
    "data": [],
    "message": "not found data",
    "code": 404,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "min_price": [
            "The min price format is invalid."
        ],
        "max_price": [
            "The max price format is invalid."
        ],
        "category_id": [
            "The category id must not be greater than 250 characters."
        ]
    }
}
</pre>
</td>
</tr>
</table>


___
## Auth:

### Register 

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>It shouldn't be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Register</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>name-email-password</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>auth/register</td>
</tr>
<tr>
<th style="text-align:start">Response success Format</th>
<td>
<pre>
{
    "data": {
        "id": 1,
        "name": "mostafa",
        "email": "mo@mo.com",
        "created_at": "2022-11-12T13:18:31.000000Z",
        "updated_at": "2022-11-12T13:18:31.000000Z"
    },
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC8xMjcuMC4wLjE6ODAwMFwvYXBpXC9hdXRoXC9yZWdpc3RlciIsImlhdCI6MTY2ODI1OTExMiwiZXhwIjoxNjY4MjYyNzEyLCJuYmYiOjE2NjgyNTkxMTIsImp0aSI6IkJZMXZZS05YdkhxaVgyM2oiLCJzdWIiOjEsInBydiI6IjIzYmQ1Yzg5NDlmNjAwYWRiMzllNzAxYzQwMDg3MmRiN2E1OTc2ZjcifQ.rldsbytiLjNygNGeBAACWErL-3eGeomusdNJC2X1vz0",
    "message": "User created successfully",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>The email has already</strong>
{
    "data": "",
    "token": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "email": [
            "The email has already been taken."
        ]
    }
}
<hr></hr>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "token": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "email": [
            "The email field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>

___

### Login 

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>Must be registered</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Login</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>email-password</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>auth/login</td>
</tr>
<tr>
<th style="text-align:start">Response success Format</th>
<td>
<pre>
<strong>unregistered</strong>
{
    "data": "",
    "token": false,
    "message": "Unauthorized",
    "code": 401,
    "errors": ""
}
<hr></hr>
<strong> Successfully log in </strong>
{
    "data": {
        "id": 1,
        "name": "mostafa",
        "email": "mo@mo.com",
        "created_at": "2022-11-12T13:18:31.000000Z",
        "updated_at": "2022-11-12T13:18:31.000000Z"
    },
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC8xMjcuMC4wLjE6ODAwMFwvYXBpXC9hdXRoXC9sb2dpbiIsImlhdCI6MTY2ODI2MzIyMCwiZXhwIjoxNjY4MjY2ODIwLCJuYmYiOjE2NjgyNjMyMjAsImp0aSI6Ik1rdDRlZ3piaXFTNU9sYjciLCJzdWIiOjEsInBydiI6IjIzYmQ1Yzg5NDlmNjAwYWRiMzllNzAxYzQwMDg3MmRiN2E1OTc2ZjcifQ.g4sQEdhE3eCnOEScbKUxtbfjwhdj8Gq5CkO1ILJqqWc",
    "message": "success",
    "code": 200,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": "",
    "token": "",
    "message": "fail",
    "code": 422,
    "errors": {
        "email": [
            "The email field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>


___

### Logout 

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>Must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Logout</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>auth/logout</td>
</tr>
<tr>
<th style="text-align:start">Response success Format</th>
<td>
<pre>
{
    "data": "",
    "token": "",
    "message": "Successfully logged out",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Refresh 

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>Must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Refresh</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>auth/refresh</td>
</tr>
<tr>
<th style="text-align:start">Response success Format</th>
<td>
<pre>
{
    "data": {
        "id": 1,
        "name": "mostafa",
        "email": "mo@mo.com",
        "created_at": "2022-11-12T13:18:31.000000Z",
        "updated_at": "2022-11-12T13:18:31.000000Z"
    },
    "token": "",
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>


___
## Carts:

### Index

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>get all carts</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>carts</td>
</tr>
<tr>
<th style="text-align:start">Format response success</th>
<td>
<pre>
<strong>Cart is empty</strong>
{
    "data": [],
    "message": "",
    "code": 200,
    "errors": []
}
<hr></hr>
<strong>Cart is full</strong>
{
    "data": [
        {
            "id": 8,
            "name": "Paige Dooley",
            "quantity": 3,
            "image": "https://via.placeholder.com/350",
            "price": 422,
            "offer": 35,
            "user_id": 1,
            "created_at": "2022-11-12T11:57:24.000000Z",
            "updated_at": "2022-11-12T11:57:24.000000Z"
        }
    ],
    "message": "",
    "code": 200,
    "errors": []
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Store

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>add new product to cart</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token-quantity-prod_id</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>addtocart/{productid}</td>
</tr>
<tr>
<th style="text-align:start">Format response success</th>
<td>
<pre>
{
    "data": {
        "id": 9,
        "name": "Estell Harris MD",
        "quantity": "3",
        "image": "https://via.placeholder.com/350",
        "price": 481,
        "offer": 20,
        "user_id": 1,
        "created_at": "2022-11-12T12:01:51.000000Z",
        "updated_at": "2022-11-12T12:01:51.000000Z"
    },
    "message": "success",
    "code": 201,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>Data not available</strong>
{
    "data": [],
    "message": "data is not available",
    "code": 404,
    "errors": ""
}
<hr>
<strong>The product is already in the cart</strong>
{
    "data": [],
    "message": "The product is already in the cart",
    "code": 404,
    "errors": ""
}
<hr></hr>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": [],
    "message": "fail",
    "code": 422,
    "errors": {
        "quantity": [
            "The quantity format is invalid."
        ]
    }
}
</pre>
</td>
</tr>
</table>


___

### Update

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Update the specified product quantity</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token-_method=put-prod_id-quantity</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>updateproductincart/{cartid}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 8,
        "name": "Paige Dooley",
        "quantity": "2",
        "image": "https://via.placeholder.com/350",
        "price": 422,
        "offer": 35,
        "user_id": 1,
        "created_at": "2022-11-12T11:57:24.000000Z",
        "updated_at": "2022-11-12T12:14:34.000000Z"
    },
    "message": "success",
    "code": 202,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": [],
    "message": "fail",
    "code": 422,
    "errors": {
        "quantity": [
            "The quantity format is invalid."
        ]
    }
}
</pre>
</td>
</tr>
</table>

___

### Destroy

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Remove the product from the selected shopping cart</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token-cart_id</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>delete</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>deletefromcart/{cartid}</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": {
        "id": 8,
        "name": "Paige Dooley",
        "quantity": 2,
        "image": "https://via.placeholder.com/350",
        "price": 422,
        "offer": 35,
        "user_id": 1,
        "created_at": "2022-11-12T11:57:24.000000Z",
        "updated_at": "2022-11-12T12:14:34.000000Z"
    },
    "message": "deleted",
    "code": 204,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

### Destroy All

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Remove all products from the selected shopping cart</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>delete</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>deletefromcartall</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>
{
    "data": [],
    "message": "deleted",
    "code": 204,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>


___
## Order:

### Index 

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Get all orders</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>name-address-email-city-phone-token</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>GET</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>getorderdata</td>
</tr>
<tr>
<th style="text-align:start">Response success Format</th>
<td>
<pre>
<strong>The order is empty</strong>
{
    "data": [],
    "message": "not found data",
    "code": 422,
    "errors": ""
}
<hr></hr>
<strong>The order is full</strong>
{
    "data": {
        "data": [
            {
                "id": 1,
                "name": "mostafa",
                "email": "mo@mo.com",
                "phone": 1122455867,
                "address": "benusufi",
                "city": "city",
                "total_price": 794,
                "status": "new",
                "order_products": [
                    {
                        "id": 1,
                        "order_id": 1,
                        "product_id": 1,
                        "quantity": 8,
                        "price": 496,
                        "offer": 20,
                        "total_price": 794,
                        "products": {
                            "id": 1,
                            "name": "Arnulfo Olson",
                            "description": "Sed occaecati non molestias ullam quis. Voluptates aut nisi itaque voluptatem. Sed saepe autem et quia. Qui veniam eum aliquid nulla laudantium aspernatur dolores. Praesentium magni assumenda facilis harum.",
                            "price": 496,
                            "offer": 20,
                            "image": "default.svg",
                            "available": "yes",
                            "category_id": 1,
                            "created_at": "2022-11-12T12:32:25.000000Z",
                            "updated_at": "2022-11-12T12:34:46.000000Z",
                            "quantity": 6
                        },
                        "created_at": "2022-11-12T12:34:46.000000Z",
                        "updated_at": "2022-11-12T12:34:46.000000Z"
                    }
                ],
                "created_at": "2022-11-12T12:34:45.000000Z",
                "updated_at": "2022-11-12T12:34:45.000000Z"
            }
        ],
        "links": {
            "first": "http://127.0.0.1:8000/api/getorderdata?page=1",
            "last": "http://127.0.0.1:8000/api/getorderdata?page=1",
            "prev": null,
            "next": null
        },
        "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 1,
            "links": [
                {
                    "url": null,
                    "label": "&laquo; Previous",
                    "active": false
                },
                {
                    "url": "http://127.0.0.1:8000/api/getorderdata?page=1",
                    "label": "1",
                    "active": true
                },
                {
                    "url": null,
                    "label": "Next &raquo;",
                    "active": false
                }
            ],
            "path": "http://127.0.0.1:8000/api/getorderdata",
            "per_page": 15,
            "to": 1,
            "total": 1
        }
    },
    "message": "success",
    "code": 202,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>No need to vaildation</td>
</tr>
</table>

___

### Store Order

<table>
<tr>
<th style="text-align:start">Authentication</th>
<td>must be</td>
</tr>
<tr>
<th style="text-align:start">use</th>
<td>Add a new order</td>
</tr>
<tr>
<th style="text-align:start">parameter</th>
<td>token</td>
</tr>
<tr>
<th style="text-align:start">method</th>
<td>POST</td>
</tr>
<tr>
<th style="text-align:start">url</th>
<td>order</td>
</tr>
<tr>
<th style="text-align:start">Response success format</th>
<td>
<pre>

<strong>Cart is empty</strong>
{
    "data": [],
    "message": "Your cart is empty",
    "code": 422,
    "errors": ""
}
<hr>
<strong>Cart is full</strong>
{
    "data": {
        "id": 2,
        "name": "mostafa",
        "email": "mo@mo.com",
        "phone": "01122455867",
        "address": "benusufi",
        "city": "city",
        "total_price": 793.6,
        "status": null,
        "order_products": [
            {
                "id": 2,
                "order_id": 2,
                "product_id": 1,
                "quantity": 8,
                "price": 496,
                "offer": 20,
                "total_price": 794,
                "products": {
                    "id": 1,
                    "name": "Arnulfo Olson",
                    "description": "Sed occaecati non molestias ullam quis. Voluptates aut nisi itaque voluptatem. Sed saepe autem et quia. Qui veniam eum aliquid nulla laudantium aspernatur dolores. Praesentium magni assumenda facilis harum.",
                    "price": 496,
                    "offer": 20,
                    "image": "default.svg",
                    "available": "no",
                    "category_id": 1,
                    "created_at": "2022-11-12T12:32:25.000000Z",
                    "updated_at": "2022-11-12T12:45:50.000000Z",
                    "quantity": -2
                },
                "created_at": "2022-11-12T12:45:50.000000Z",
                "updated_at": "2022-11-12T12:45:50.000000Z"
            }
        ],
        "created_at": "2022-11-12T12:45:49.000000Z",
        "updated_at": "2022-11-12T12:45:49.000000Z"
    },
    "message": "success",
    "code": 202,
    "errors": ""
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Error-Format</th>
<td>
<pre>
<strong>object not found</strong>
{
    "data": "",
    "message": "fail",
    "code": 404,
    "errors": "object not found"
}
<hr></hr>
<strong>Method Not Allowed</strong>
{
    "data": "",
    "message": "fail",
    "code": 405,
    "errors": "Method Not Allowed"
}
<hr></hr>
<strong>Unauthenticated</strong>
{
    "message": "Unauthenticated."
}
</pre>
</td>
</tr>
<tr>
<th style="text-align:start">Vaildation</th>
<td>
<pre>
{
    "data": [],
    "message": "fail",
    "code": 422,
    "errors": {
        "name": [
            "The name field is required."
        ],
        "email": [
            "The email field is required."
        ],
        "address": [
            "The address field is required."
        ]
    }
}
</pre>
</td>
</tr>
</table>
