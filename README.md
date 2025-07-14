# arf

ARF - API Request/Response Formats

## Responses

20X responses should return with an outer object label, eg:

```json
{
  "product": {
    "id": "123",
    "name": "Ice cream"
  }
}
```

For multiple items being returned:

```json
{
  "products": [
    {
      "id": "123",
      "name": "Ice cream"
    },
    {
      "id": "456",
      "name": "chocolate bar"
    },
  ]
}
```

## Error Responses

This matches up with JavaScript error.message. 

```json
{
  "error": {
    "message": "something bad happened",
    "status": 400
  }
}
```

* Status is optional, can read the response.status if needed, but nice to have in the error object.
* We use `status` here instead of `code` so it matches `Response.status`. 
