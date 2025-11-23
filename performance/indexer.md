# Indexer Performance SPL

### Indexing throughput

```spl
index=_internal source=*metrics.log group=thruput
| timechart sum(kb) by series
```

### Queue size monitoring

```spl
index=_internal source=*metrics.log group=queue
| timechart avg(current_size) by name
```
