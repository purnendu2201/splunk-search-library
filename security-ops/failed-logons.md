# Failed Login Attempts – SPL

### Count failed logins by user

```spl
index=your_auth sourcetype=your_auth action=failure
| stats count by user
```


### Timechart of failures

```spl
index=your_auth action=failure
| timechart span=5m count
```

