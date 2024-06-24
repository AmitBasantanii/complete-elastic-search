# 1

# How the `keyword` data type works

## Testing the `keyword` analyzer

```

POST /_analyze
{
  "text": "2 guys walk into   a bar, but the third... DUCKS! :-)",
  "analyzer": "standard"
}

POST /_analyze
{
  "text": "2 guys walk into   a bar, but the third... DUCKS! :-)",
  "analyzer": "keyword"
}

POST /_analyze
{
  "text": "2 guys walk into   a bar, but the third... DUCKS! :-)",
  "char_filter" : [],
  "tokenizer" : "standard",
  "filter" : ["lowercase"]
}
```
