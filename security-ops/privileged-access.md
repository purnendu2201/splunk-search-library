# Privileged Access – SPL

### Detect sudo usage

```spl
index=your_index command=sudo
| stats count by user host
```

### Identify unusual elevated access

```spl
index=your_index command=sudo
| stats count by user
| where count > 10
```
