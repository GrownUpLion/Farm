# Farm Api

- [Farm API](#Farm-api)
  - [Create animal](#create-animal)
    - [Create animal Request](#create-animal-request)
    - [Create animal Response](#create-animal-response)
  - [Get animal](#get-animal)
    - [Get animal Request](#get-animal-request)
    - [Get animal Response](#get-animal-response)
  - [Update animal](#update-animal)
    - [Update animal Request](#update-animal-request)
    - [Update animal Response](#update-animal-response)
  - [Delete animal](#delete-animal)
    - [Delete animal Request](#delete-animal-request)
    - [Delete animal Response](#delete-animal-response)

## Create animal

### Create animal Request

```js
POST /animals
```

```json
      {
        "Sex": "Female",
        "AnimalType": "Cow",
        "Feedings": [
          {
            "DateTime": "2021-10-01T10:32:00",
            "Amount": 25
          },
          {
            "DateTime": "2021-10-31T18:42:00",
            "Amount": 26
          }
        ],
        "Milkings": [
          {
            "DateTime": "2021-10-01T09:38:00",
            "Amount": 28
          },
          {
            "DateTime": "2021-10-01T17:01:00",
            "Amount": 0
          },
        ]
      }
```

### Create animal Response

```js
201 Created
```

```yml
Location: {{host}}/animals/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "Sex": "Female",
    "AnimalType": "Cow",
    "Feedings": [
      {
        "DateTime": "2021-10-01T10:32:00",
        "Amount": 25
      },
      {
        "DateTime": "2021-10-31T18:42:00",
        "Amount": 26
      }
    ],
    "Milkings": [
      {
        "DateTime": "2021-10-01T09:38:00",
        "Amount": 28
      },
      {
        "DateTime": "2021-10-01T17:01:00",
        "Amount": 0
      },
    ]
}
```

## Get animal

### Get animal Request

```js
GET /animals/{{id}}
```

### Get animal Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "Sex": "Female",
    "AnimalType": "Cow",
    "Feedings": [
      {
        "DateTime": "2021-10-01T10:32:00",
        "Amount": 25
      },
      {
        "DateTime": "2021-10-31T18:42:00",
        "Amount": 26
      }
    ],
    "Milkings": [
      {
        "DateTime": "2021-10-01T09:38:00",
        "Amount": 28
      },
      {
        "DateTime": "2021-10-01T17:01:00",
        "Amount": 0
      },
    ]
}
```

## Update animal

### Update animal Request

```js
PUT /animals/{{id}}
```

```json
{
    "Sex": "Female",
    "AnimalType": "Cow",
    "Feedings": [
      {
        "DateTime": "2021-10-01T10:32:00",
        "Amount": 25
      },
      {
        "DateTime": "2021-10-31T18:42:00",
        "Amount": 26
      }
    ],
    "Milkings": [
      {
        "DateTime": "2021-10-01T09:38:00",
        "Amount": 28
      },
      {
        "DateTime": "2021-10-01T17:01:00",
        "Amount": 0
      },
    ]
}
```

### Update animal Response

```js
204 No Content
```

or

```js
201 Updated
```

```yml
Location: {{host}}/animals/{{id}}
```

## Delete animal

### Delete animal Request

```js
DELETE /animals/{{id}}
```

### Delete animal Response

```js
204 No Content
```
