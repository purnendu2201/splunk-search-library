# Missing Fields – SPL

### Count events missing a field

```spl
index=your_index
| where isnull(field_you_expect)
| stats count
```

### Field distribution

```spl
index=your_index
| top field_you_expect
```
