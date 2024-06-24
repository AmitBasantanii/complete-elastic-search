# Upserts

# if the document already exists, a script is run, and if it doesn't a new document is created

# updating the id with 101, just to create the new document

```
# creating first
GET /products/_doc/101

# upserts
POST /products/_update/101
{
  "script": {
    "source": "ctx._source.in_stock++"
  },
  "upsert": {
    "name": "Blender",
    "price": 399,
    "in_stock": 5
  }
}
```
