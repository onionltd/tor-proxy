# tor-proxy

Installs and starts Tor and exposes SOCKS5 proxy on port 9050.

## Usage

```
on: [push]
jobs:
  tor_test:
    runs-on: ubuntu-latest
    name: curl data from the Tor network
    steps:
    - uses: onionltd/tor-proxy@v1
    - run: curl http://onions53ehmf4q75.onion
      env: 
        http_proxy: "socks5h://localhost:9050"
        https_proxy: "socks5h://localhost:9050"
```
