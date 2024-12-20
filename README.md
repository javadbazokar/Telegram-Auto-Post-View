
# Telegram Auto Views 2024

### Features
- **Asynchronous Operation**: Optimized for performance and speed.
- **Full Proxy Support**: HTTP/S, SOCKS4, SOCKS5 proxies are fully supported.
- **Auto Proxy Scraping**: No need to manually collect proxies – the tool scrapes them automatically.

---

### Arguments Example + Modes

Below are different ways to use the tool, depending on your preferred mode and proxy source.

#### 1. **Auto Scraping Mode** (Auto Proxy "PROXYLESS")

This mode automatically scrapes proxies from various sources, ensuring you don't need to manually provide any. It runs continuously, automatically refreshing proxies after each loop.

```bash
# Usage example: Send views to the channel @teleview, post number 4
# e.g: https://t.me/teleview/4

teleview.py --mode auto --channel teleview --post 4
```

---

#### 2. **Load Proxies From File**

If you have a list of proxies saved in a `.txt` file, you can use this mode to load and use them. Simply specify your file path.

```bash
# Usage example: Load HTTP proxies from the file 'http.txt' and send views to @teleview post number 4

teleview.py --type http --mode list --proxy http.txt --channel teleview --post 4
```

---

#### 3. **Using Rotating Proxies**

If you have proxies that need to rotate for each request, you can use this mode to apply rotating proxies with authentication.

```bash
# Usage example: Use rotating HTTP proxies with authentication and send views to @teleview post number 4

teleview.py -t http -m rotate -p user:password@ip:port -c teleview -pt 4
```

---

### Notes
- **Mode Options**:  
  - `auto`: Scrapes proxies automatically.
  - `list`: Uses a list of proxies from a file.
  - `rotate`: Uses rotating proxies.
  
- **Proxy Types**:  
  - `http`: Standard HTTP proxies.
  - `socks4`, `socks5`: SOCKS4 or SOCKS5 proxies.

- **Channel & Post**:  
  - `--channel`: Specify the Telegram channel.
  - `--post`: Specify the post number you want to send views to (e.g., `4` for `https://t.me/teleview/4`).

---

### Contact & Support
For issues or feedback, feel free to open an issue.

---
