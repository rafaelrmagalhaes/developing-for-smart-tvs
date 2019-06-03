# LG
### Overview
LG's Smart TVs have their operating system `WebOS` or `Netcast`. Nowadays, `Netcast` is already a legacy system and
is avoided maintenance even by the manufacturer. A nice advise is slowly avoid supporting these type of Smart TVs.

### Operating System and Web Engines
| OS  | Realese Year |  Engine |
| ------------- | ---------------- | ------- |
| WebOS 4.x | 2019 | Chromium 53 | 
|  | 2018 | Chromium 53 | 
| WebOS 3.x | 2017 | Chromium 38 |
|  | 2016 | Chromium 38 |
| WebOS 2.x | 2015 | WebKit 538.2 |
| Netcast 4.5 LM14 | 2015 | WebKit 537.1 |
| Netcast 4.5 M13 | 2015 | WebKit 537.1 |
| WebOS 1.x | 2014 | WebKit 537.41 |
| Netcast 4.5 LM14 | 2014 | WebKit 537.1 |
| Netcast 4.5 M13 | 2014 | WebKit 537.1 |
| Netcast 4.0 H13 | 2013 | WebKit 537.1+ (*Diff_NC3.0) |
| Netcast 4.0 M13 | 2013 | Webkit 537.1+ (*Diff_NC3.0)  |
| Netcast 3.0 H12 | 2012 | Webkit 534.26+ (*Diff_NC2.0) |
| Netcast 3.0 M12 | 2012 | Webkit 534.26+ (*Diff_NC2.0) |
| Netcast 2.0 | 2011 | Webkit 531.2+  |

# WebOS

## Technical Information
Everything about LG Development can be find in their [website](http://webostv.developer.lge.com/discover/specifications/web-engine/). This is just a compilation of important things
to keep updated.

## Architecture
![Architecture of WebOS TVs](http://webostv.developer.lge.com/download_file/view_inline/5990/)

### Agent Strings
<strong>WebOS TV 4.x</strong>
```
Mozilla/5.0 (Web0S; Linux/SmartTV) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/53.0.2785.34 Safari/537.36 WebAppManager
```

<strong>WebOS TV 3.x</strong>
```
Mozilla/5.0 (Web0S; Linux/SmartTV) AppleWebKit/537.36 (KHTML, like Gecko) QtWebEngine/5.2.1 Chrome/38.0.2125.122 Safari/537.36 WebAppManager
```

<strong>WebOS TV 2.x</strong>
```
Mozilla/5.0 (Web0S; Linux/SmartTV) AppleWebKit/538.2 (KHTML, like Gecko) Large Screen WebAppManager Safari/538.2
```

<strong>WebOS TV 1.x</strong>
```
Mozilla/5.0 (Web0S; Linux/SmartTV) AppleWebKit/537.41 (KHTML, like Gecko) Large Screen WebAppManager Safari/537.41
```

### TSL/SSL
| Versions  | webOS 1.x/2.x |  webOS 3.x | webOS 4.x |
| ------------- | ---------------- | --------- | ---- |
| TLS v1.2 | Supported | Supported | Supported |
| TLS v1.1 | Supported | Supported | Supported |
| TLS v1.0¹ | Supported | Supported | Supported |
| SSL v3.0² | Not Supported | Not Supported | Not Supported |
| SSL v2.0³ | Not Supported | Not Supported | Not Supported |

```
¹ - Upgrade of SSL v3.0
² - Deprecated in June 2015 by RFC 7568
² - Deprecated in 2011 by RFC 6176
```
