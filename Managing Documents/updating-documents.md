# Updating documents

## Updating an existing field

```
POST /products/_update/100
{
  "doc": {
    "in_stock": 3
  }
}
```

# Checking if product got updated or not

GET /products/\_doc/100

## Adding a new field

_Yes, the syntax is the same as the above. ;-)_

```
POST /products/_update/100
{
  "doc": {
    "tags": ["electronics"]
  }
}
```
