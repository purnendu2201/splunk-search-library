# Search Head Performance SPL

### Long-running searches

```spl
index=_audit action=search info=completed
| where duration > 30
| stats max(duration) avg(duration) by user
```

### Skipped searches

```spl
index=_internal sourcetype=scheduler status=skipped
| stats count by savedsearch_name
```

