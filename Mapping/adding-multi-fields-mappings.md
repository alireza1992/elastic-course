# Adding multi-fields mappings

## Adding mappings

```
PUT /product/_mapping
{
  "properties": {
    "description": {
      "type": "text"
    },
    "name": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword"
        }
      }
    },
    "tags": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword"
        }
      }
    }
  }
}
```

## Retrieving mapping

```
GET /product/_mapping
```