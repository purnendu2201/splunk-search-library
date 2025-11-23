# Null Values – SPL

### Check null vs non-null

```spl
index=your_index
| eval status=if(isnull(field1),"null","present")
| stats count by status
```

### Detect malformed logs

```spl
index=your_index
| where like(_raw,"%error%") OR like(_raw,"%fail%")
```
