# Docs
Docs for mljar-supervised available at https://supervised.mljar.com

### Development

```
mkdocs serve
```

### Deploy

```
mkdocs build
aws s3 sync site/ s3://supervised.mljar.com
```