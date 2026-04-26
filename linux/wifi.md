### start wifi

```bash
iwctl station list
```

### connect to saved network

```bash
iwctl station wlan0 connect "Videotron"
```

### connect to new network

```bash
iwctl
station wlan0 scan
station wlan0 connect "Bell"
```
