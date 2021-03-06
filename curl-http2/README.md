curl-http2
==========

[![](https://images.microbadger.com/badges/version/badouralix/curl-http2.svg)](https://microbadger.com/images/badouralix/curl-http2 "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/badouralix/curl-http2.svg)](https://microbadger.com/images/badouralix/curl-http2 "Get your own image badge on microbadger.com")


This repository contains a **Dockerfile** for [curl](https://curl.haxx.se/) with http2 support.

See the repo on [Docker Hub](https://hub.docker.com/r/badouralix/curl-http2/).


## Installation

### Automated build

```bash
$ docker pull badouralix/curl-http2
```

### Self build

```bash
$ git clone https://github.com/badouralix/dockerfiles.git
$ cd dockerfiles/curl-http2/<BASE_IMAGE>
$ docker build -t $USER-local/curl-http2:<BASE_IMAGE> .
```


## Usage

```
$ docker run -t --rm badouralix/curl-http2 -I https://nghttp2.org/

HTTP/2 200
date: Wed, 12 Apr 2017 00:26:57 GMT
content-type: text/html
last-modified: Sun, 09 Apr 2017 13:25:12 GMT
etag: "58ea3638-19ff"
accept-ranges: bytes
content-length: 6655
x-backend-header-rtt: 0.001404
strict-transport-security: max-age=31536000
server: nghttpx
via: 2 nghttpx
x-frame-options: SAMEORIGIN
x-xss-protection: 1; mode=block
x-content-type-options: nosniff
```


## Tips and tricks

In your shell rc dotfile, you could add an `alias 'curl-http2'='docker run -t --rm badouralix/curl-http2'`
so that you would just have to run :

```
$ curl-http2 -I https://nghttp2.org/
```


## Tags

All images are built with [`nghttp2 v1.26.0`](https://github.com/nghttp2/nghttp2/releases/tag/v1.26.0) and [`curl 7.56.0`](https://github.com/curl/curl/releases/tag/curl-7_56_0).

 - `latest`, `alpine` : image based on `alpine:3.6`
 - `debian` : image based on `debian:stretch`


## Versions, protocols and features

### Alpine

```
curl 7.56.0 (x86_64-pc-linux-gnu) libcurl/7.56.0 OpenSSL/1.0.2k zlib/1.2.11 nghttp2/1.26.0
Release-Date: 2017-10-04
Protocols: dict file ftp ftps gopher http https imap imaps pop3 pop3s rtsp smb smbs smtp smtps telnet tftp
Features: AsynchDNS IPv6 Largefile NTLM NTLM_WB SSL libz TLS-SRP HTTP2 UnixSockets HTTPS-proxy
```

### Debian

```
curl 7.56.0 (x86_64-pc-linux-gnu) libcurl/7.56.0 OpenSSL/1.1.0f zlib/1.2.8 libpsl/0.17.0 (+libidn2/0.16) libssh2/1.7.0 nghttp2/1.26.0 librtmp/2.3
Release-Date: 2017-10-04
Protocols: dict file ftp ftps gopher http https imap imaps ldap ldaps pop3 pop3s rtmp rtsp scp sftp smb smbs smtp smtps telnet tftp
Features: AsynchDNS IPv6 Largefile GSS-API Kerberos SPNEGO NTLM NTLM_WB SSL libz TLS-SRP HTTP2 UnixSockets HTTPS-proxy PSL
```


## License

Unless explicitly stated to the contrary, all contents licensed under the [WTFPL](https://github.com/badouralix/dockerfiles/blob/master/LICENSE).

