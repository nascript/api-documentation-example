# api-documentation-example

# My Happiness API documentation

### Base Local URL

```url
http://localhost:3001/
```

## Article Feature

### Add Article (Role Admin)

`POST /admin/v1/myhappiness/articles/add`

Add new article data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Request Body**

- `name`, string | required | min(0) | max(100) => article name
- `tags`, array | required => article tag
- `categories`, array | required => article categories
- `description`, string | required => article description
- `content`, string | required => article content
- `pathPhotoUrl`, array | required => article pathPhotoUrl
- `publishAt`, number | required => article publishAt
- `originUrl`, string | required => article originUrl
- `originAuthor`, array | required => article originAuthor
- `likeStatur`, array | required => article likeStatur
- `read` array | required => article read

**Sample Request**

```json
{
  "name": "jumat 7",
  "tags": ["89dcab523-3ed2-471f-aacc-d8f79b64a9e3"],
  "categories": ["371xab523-2ed2-473f-avcc-d2f79b64a9e3"],
  "description": "from jumat desc 7",
  "content": "from jumat postman content 7",
  "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
  "publishAt": 1643681160144,
  "originUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
  "originAuthor": ["tionpostman"],
  "likeStatus": ["62e0eeb9-d07e-461e-b39a-5b7ff68565b4"],
  "read": ["62e0eeb9-d07e-461e-b39a-5b7ff68565b4"]
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 1,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"content\" is required"
    }
}
```

</details>

### List Article (Role Admin)

`GET /admin/v1/myhappiness/articles/my/list`

List Article

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 1,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },

    more....
}
```

<!-- **Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"content\" is required"
    }
}
``` -->

</details>

### List Article (Role Customer)

`GET /admin/v1/myhappiness/articles/list`

List Article

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 1,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },

    more....
}
```

<!-- **Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"content\" is required"
    }
}
``` -->

</details>

### Article Detail

`GET /admin/v1/myhappiness/articles/:id`

Article Detail

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 1,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },
}
```

**Error Response**

- Not Found

```json
HTTP/1.1 404 Not Found
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "article not found"
    }
}
```

</details>

### Update Article (Role Admin)

`POST /v1/myhappiness/articles/update/:id`

Update Article

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Body Request**

- `name`, string | required | min(0) | max(100) => article name
- `tags`, array | required => article tag
- `categories`, array | required => article categories
- `description`, string | required => article description
- `content`, string | required => article content
- `pathPhotoUrl`, array | required => article pathPhotoUrl
- `publishAt`, number | required => article publishAt
- `originUrl`, string | required => article originUrl
- `originAuthor`, array | required => article originAuthor
- `likeStatur`, array | required => article likeStatur
- `read` array | required => article read

**Sample Request**

```json
{
  "name": "jumat 7",
  "tags": ["89dcab523-3ed2-471f-aacc-d8f79b64a9e3"],
  "categories": ["371xab523-2ed2-473f-avcc-d2f79b64a9e3"],
  "description": "from jumat desc 7",
  "content": "from jumat postman content 7",
  "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
  "publishAt": 1643681160144,
  "originUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
  "originAuthor": ["tionpostman"],
  "likeStatus": ["62e0eeb9-d07e-461e-b39a-5b7ff68565b4"],
  "read": ["62e0eeb9-d07e-461e-b39a-5b7ff68565b4"]
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 1,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },

}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"content\" is required"
    }
}
```

- Not Found

```json
HTTP/1.1 404 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "article not found"
    }
}
```

</details>

### Update Article Data Active (Role Admin)

`GET /admin/v1/myhappiness/articles/activate/:id`

Update Article `dataStatus 1 = activate`

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 1,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },

}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article not found"
    }
}
```

- Not Found

```json
HTTP/1.1 404 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "article not found"
    }
}
```

</details>

### Update Article Data Active (Role Admin)

`GET /admin/v1/myhappiness/articles/deactivate/:id`

Update Article `dataStatus 2 = Inactive`

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 2,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },

}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article not found"
    }
}
```

- Not Found

```json
HTTP/1.1 404 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "article not found"
    }
}
```

</details>

### Update Article Data Active (Role Admin)

`GET /admin/v1/myhappiness/articles/deactivate/:id`

Update Article `dataStatus 3 = Remove`

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticle": {
            "id": "5c372a2d-28ce-4358-886f-46fc3d8f06e0",
            "articleName": "jumat 7",
            "articleTags": [
                {
                    "id": "89dcab523-3ed2-471f-aacc-d8f79b64a9e3",
                    "tagName": "heart"
                }
            ],
            "articleCategories": [
                {
                    "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                    "categoryName": "Kardiologi"
                }
            ],
            "articleDescription": "from jumat desc 7",
            "articleContent": "from jumat postman content 7",
            "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "articlePublishAt": 1643681160144,
            "articleOriginUrl": "https://www.halodoc.com/artikel/11-penyakit-yang-ditangani-dokter-spesialis-penyakit-dalam 2",
            "articleOriginAuthor": [
                "tionpostman"
            ],
            "articleLikeStatus": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "articleRead": [
                "62e0eeb9-d07e-461e-b39a-5b7ff68565b4"
            ],
            "dataStatus": 3,
            "audit": {
                "createdAt": "2022-02-04T03:46:59.105Z",
                "updatedAt": "2022-02-04T03:46:59.105Z",
                "createdBy": "system",
                "updatedBy": "system"
            }
        }
    },

}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article not found"
    }
}
```

- Not Found

```json
HTTP/1.1 404 Bad Request
Content-Type: application/json
{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "article not found"
    }
}
```

</details>

### Image Article

`GET /admin/v1/myhappiness/articles/photo/presigned/*extension`

get URL aws

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "signedUrl": "https://nadi-cdn.s3.ap-southeast-1.amazonaws.com/articles/dc6ade98801841fb8897bd539059e809.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIA6HIV5YVRJQYYRTGN%2F20220204%2Fap-southeast-1%2Fs3%2Faws4_request&X-Amz-Date=20220204T041144Z&X-Amz-Expires=3600&X-Amz-Signature=c05449895cb709c47c6984a1f09fbb465da9364bea1a1c7455b0c15f59838149&X-Amz-SignedHeaders=host&x-amz-acl=public-read&x-id=PutObject",
        "fileUrl": "https://nadi-cdn.s3.ap-southeast-1.amazonaws.com/articles/dc6ade98801841fb8897bd539059e809.png"
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"ext\" must be one of [jpg, jpeg, png]"
    }
}
```

</details>

### Delete Image Article

`POST /admin/v1/myhappiness/articles/photo/delete`

Delete photo assign in aws

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "message": "Image deleted successfully"
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"key\" is required"
    }
}
```

</details>

## Article Categories Feature

### Add Article category (Role Admin)

`POST /v1/admin/myhappiness/article-categories/add`

Add new article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Request Body**

- `name`, string | required => article name
- `photoProfile`, string | required => Thumbnail of category
- `parent`, string | null => parentId
- `articles`, array => list articles of category
- **Sample Request**

```json
{
  "name": "Hair",
  "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
  "parent": ""
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "insertedArticleCategory": {
            "id": "641f5b25-da5e-4be6-bf81-bd3607db5b39",
            "parentId": null,
            "categoryName": "Hair",
            "childrens": [],
            "articles": [],
            "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "dataStatus": 1,
            "audit": {
                "createdAt": 1644235753490,
                "createdBy": "faker-admin",
                "updatedAt": 1644235753490,
                "updatedBy": "faker-admin"
            },
            "articleTotal": 0
        }
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 400 Bad Request
Content-Type: application/json
{
    "code": 400,
    "success": false,
    "error": {
        "name": "ValidationError",
        "message": "\"name\" is required"
    }
}
```

</details>

### List Article category (Role Admin)

`GET v1/admin/myhappiness/article-categories/list`

List All article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "articleCategories": [
            {
                "id": "d03b019e-8b9f-4b6e-b654-edd499616eb9",
                "parentId": null,
                "categoryName": "Nose",
                "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
                "childrens": [],
                "articles": [
                    {
                        "id": "0049760d-235b-487d-b7ad-47fff46d9da1",
                        "articleName": "rabu",
                        "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                    }
                ],
                "dataStatus": 1,
                "audit": {
                    "createdAt": 1644234421141,
                    "createdBy": "faker-admin",
                    "updatedAt": 1644234421141,
                    "updatedBy": "faker-admin"
                },
                "articleTotal": 1
            },
            {
                "id": "205a31b2-371e-48a8-b0a4-9e8e2142ff43",
                "parentId": null,
                "categoryName": "Nose",
                "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
                "childrens": [],
                "articles": [],
                "dataStatus": 1,
                "audit": {
                    "createdAt": 1644234338152,
                    "createdBy": "faker-admin",
                    "updatedAt": 1644234338152,
                    "updatedBy": "faker-admin"
                },
                "articleTotal": 0
            },
            {
                "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
                "parentId": null,
                "categoryName": "Kardiologi update",
                "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
                "childrens": [],
                "articles": [
                    {
                        "id": "0049760d-235b-487d-b7ad-47fff46d9da1",
                        "articleName": "rabu",
                        "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                    },
                    {
                        "id": "b43b153a-721b-40f2-ab70-5c7fb828d917",
                        "articleName": "senunu",
                        "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                    }
                ],
                "dataStatus": 2,
                "audit": {
                    "createdAt": 1643678491702,
                    "updatedAt": 1644238343073,
                    "updatedBy": "faker-admin"
                },
                "articleTotal": 2
            },
            {
                "id": "3723fb523-2dd2-477f-aagc-d8f74b64a9e3",
                "parentId": null,
                "categoryName": "Reumatologi",
                "photoProfile": "https://cdn.pixabay.com/photo/2015/05/13/13/53/skull-765477_1280.jpg",
                "childrens": [],
                "articles": [],
                "dataStatus": 1,
                "audit": {
                    "createdAt": 1643678491702,
                    "updatedAt": 1643678491702
                },
                "articleTotal": 0
            }
        ],
        "total": 4,
        "count": 4,
        "skip": 0,
        "limit": 10
    }
}
```

</details>

### List Article category (Role Customer)

`GET v1/admin/myhappiness/article-categories/list`

List All article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "articleCategories": [
            {
                "id": "d03b019e-8b9f-4b6e-b654-edd499616eb9",
                "parentId": null,
                "categoryName": "Nose",
                "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
                "childrens": [],
                "dataStatus": 1
            },
            {
                "id": "205a31b2-371e-48a8-b0a4-9e8e2142ff43",
                "parentId": null,
                "categoryName": "Nose",
                "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
                "childrens": [],
                "dataStatus": 1
            },
            {
                "id": "3723fb523-2dd2-477f-aagc-d8f74b64a9e3",
                "parentId": null,
                "categoryName": "Reumatologi",
                "photoProfile": "https://cdn.pixabay.com/photo/2015/05/13/13/53/skull-765477_1280.jpg",
                "childrens": [],
                "dataStatus": 1
            }
        ],
        "total": 3,
        "count": 3,
        "skip": 0,
        "limit": 10
    }
}
```

</details>

### Detail Article category (Role Admin)

`GET v1/admin/myhappiness/article-categories/detail/:categoryId`

Detail article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "articleCategory": {
            "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
            "parentId": null,
            "categoryName": "Kardiologi update",
            "childrens": [],
            "articles": [
                {
                    "id": "0049760d-235b-487d-b7ad-47fff46d9da1",
                    "articleName": "rabu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                },
                {
                    "id": "b43b153a-721b-40f2-ab70-5c7fb828d917",
                    "articleName": "senunu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                }
            ],
            "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "dataStatus": 2,
            "audit": {
                "createdAt": 1643678491702,
                "updatedAt": 1644238343073,
                "updatedBy": "faker-admin"
            },
            "articleTotal": 2
        }
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 404 Not Found
Content-Type: application/json

{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article Category not found"
    }
}

```

</details>

### Update Article category (Role Admin)

`POST v1/admin/myhappiness/article-categories/update/categoryId`

Update article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Request Body**

- `name`, string | required => article name
- `photoProfile`, string | required => Thumbnail of category
- `parent`, string | null => parentId
- `articles`, array => list articles of category

**Sample Request**

```json
{
  "name": "Hair",
  "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
  "parent": ""
}
```

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "updatedArticleCategory": {
            "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
            "parentId": null,
            "categoryName": "Kardiologi update",
            "childrens": [],
            "articles": [
                {
                    "id": "0049760d-235b-487d-b7ad-47fff46d9da1",
                    "articleName": "rabu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                },
                {
                    "id": "b43b153a-721b-40f2-ab70-5c7fb828d917",
                    "articleName": "senunu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                }
            ],
            "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "dataStatus": 2,
            "audit": {
                "createdAt": 1643678491702,
                "updatedAt": 1644238343073,
                "updatedBy": "faker-admin"
            },
            "articleTotal": 2
        }
    }
}

```

**Error Response**

- Bad Request

```json
HTTP/1.1 404 Not Found
Content-Type: application/json

{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article Category not found"
    }
}

```

</details>

### Update `dataStatus activate` Article category (Role Admin)

`POST v1/admin/myhappiness/article-categories/activate/categoryId`

Update`dataStatus activate` article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "activatedArticleCategory": {
            "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
            "parentId": null,
            "categoryName": "Kardiologi update",
            "childrens": [],
            "articles": [
                {
                    "id": "0049760d-235b-487d-b7ad-47fff46d9da1",
                    "articleName": "rabu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                },
                {
                    "id": "b43b153a-721b-40f2-ab70-5c7fb828d917",
                    "articleName": "senunu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                }
            ],
            "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "dataStatus": 1,
            "audit": {
                "createdAt": 1643678491702,
                "updatedAt": 1644248680179,
                "updatedBy": "faker-admin",
                "activatedAt": 1644248680179,
                "activatedBy": "faker-admin"
            },
            "articleTotal": 2
        }
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 404 Not Found
Content-Type: application/json

{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article Category not found"
    }
}

```

</details>

### Update `dataStatus deactivate` Article category (Role Admin)

`POST v1/admin/myhappiness/article-categories/deactivate/categoryId`

Update`dataStatus deactivate` article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "activatedArticleCategory": {
            "id": "371xab523-2ed2-473f-avcc-d2f79b64a9e3",
            "parentId": null,
            "categoryName": "Kardiologi update",
            "childrens": [],
            "articles": [
                {
                    "id": "0049760d-235b-487d-b7ad-47fff46d9da1",
                    "articleName": "rabu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                },
                {
                    "id": "b43b153a-721b-40f2-ab70-5c7fb828d917",
                    "articleName": "senunu",
                    "pathPhotoUrl": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128..."
                }
            ],
            "photoProfile": "https://cdn.pixabay.com/photo/2016/07/24/21/01/thermometer-1539191_128...",
            "dataStatus": 2,
            "audit": {
                "createdAt": 1643678491702,
                "updatedAt": 1644248680179,
                "updatedBy": "faker-admin",
                "activatedAt": 1644248680179,
                "activatedBy": "faker-admin"
            },
            "articleTotal": 2
        }
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 404 Not Found
Content-Type: application/json

{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article Category not found"
    }
}

```

</details>

### Update `dataStatus remove` Article category (Role Admin)

`POST v1/admin/myhappiness/article-categories/delete/categoryId`

Update`dataStatus remove` article category data

<details>
    <summary>Show API</summary>

**Header Authorization**

- `Authorization`, token => user token

**Sample Request**

```json
{
    Bearer 378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f378grfuyehbcjhasdbfasldfuoa78f
}
```

**Success Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json
{
    "code": 200,
    "success": true,
    "payload": {
        "message": "Article category has been deleted"
    }
}
```

**Error Response**

- Bad Request

```json
HTTP/1.1 404 Not Found
Content-Type: application/json

{
    "code": 404,
    "success": false,
    "error": {
        "name": "NotFoundError",
        "message": "Article Category not found"
    }
}

```

</details>
