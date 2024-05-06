### WIRESHARK FILTERS


# All active TLS SNIs without noise
-  filters only packets with an SNI present
-  Drops SNIs with domains like Microsoft and Cloudflare that are most of the time, just noise.

```tls.handshake.extensions_server_name && !(tls.handshake.extensions_server_name contains "live.com") && !(tls.handshake.extensions_server_name contains "microsoft.com") && !(tls.handshake.extensions_server_name contains "googleapis.com")```
