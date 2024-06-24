# Optimistic concurrency control

## Retrieve the document (and its primary term and sequence number)

```
GET /products/_doc/100
```

## Update the `in_stock` field only if the document has not been updated since retrieving it

```
# in place of X you can put primary term and seq no as you want like 1 and 9
POST /products/_update/100?if_primary_term=X&if_seq_no=X
{
  "doc": {
    "in_stock": 123
  }
}
```
