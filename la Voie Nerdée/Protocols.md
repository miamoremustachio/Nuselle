In networking, a protocol is a set of rules for formatting and processing data.

Protocols enable computers to communicate with one another. Standardized protocols are like a common language that computers can use.

# 📄 HTTP

HTTP is a client-server application layer protocol.

Each individual request is sent to a server, which handles it and provides an answer called the _response_.

Between the client and the server there are numerous entities, collectively called [proxies](https://developer.mozilla.org/en-US/docs/Glossary/Proxy_server).
![[http-layers.jpg]]

**Basic aspects of HTTP:**

- Simple
- Human-readable
- Extensible
- Stateless, but not sessionless

## 👤 Client

The client role is primarily performed by the Web browser, but it may also be programs used by engineers and Web developers to debug their applications.

To display a Web page, the browser sends an original request to fetch the HTML document, then parses it, making additional requests corresponding to execution scripts, layout information (CSS) to display, and sub-resources contained within the page (usually images and videos).

## 🗄️ Server

_Serves_ the document as requested by the client.

Is not necessarily a single machine, but several server instances can be hosted on the same machine. With HTTP/1.1 and the [`Host`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Host) header, they may even share the same IP address.

## 🛡️ Proxy

Between the Web browser and the server, numerous computers and machines called **proxies**.

They perform numerous functions:

- caching
- filtering
- load balancing (to allow multiple servers to serve different requests)
- authentication (to control access to different resources)
- logging (allowing the storage of historical information)

## 🚚 TCP

Before a client and server can exchange an HTTP request/response pair, they must establish a TCP connection.

The default behavior of HTTP/1.0 is to open a separate TCP connection for each HTTP request/response pair.

HTTP/1.1 introduced _pipelining_ and _persistent connections:_ the underlying TCP connection can be partially controlled using the [`Connection`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Connection) header.

HTTP/2 went a step further by multiplexing messages over a single connection, helping keep the connection warm and more efficient.

## 💫 Common features

- [Caching](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
- Authentication
- Relaxing the origin constraint _(allows a document to be sourced from different domains by relaxing this strict separation on the server side)_
- [Proxy and tunneling](https://developer.mozilla.org/en-US/docs/Web/HTTP/Proxy_servers_and_tunneling)
- Sessions

## 🌊 HTTP Flow

When a client wants to communicate with a server, it performs the following steps:

1. **Open a TCP connection**
    
2. **Send an HTTP message**
    ```css
    GET / HTTP/1.1
    Host: developer.mozilla.org
    Accept-Language: fr
    ```
    
3. **Read the response sent by the server**
    
    ```css
    HTTP/1.1 200 OK
    Date: Sat, 09 Oct 2010 14:28:02 GMT
    Server: Apache
    Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
    ETag: "51142bc1-7449-479b075b2891b"
    Accept-Ranges: bytes
    Content-Length: 29769
    Content-Type: text/html
    
    <!doctype html>… (here come the 29769 bytes of the requested web page)
    ```
    
4. **Close or reuse the connection for further requests**
    

## ✉️ Messages
🟡 Request:
![[http-request.jpg]]

🟢 Response:
![[http-response.jpg]]


> **Sources:**
> - https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/
> - https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview

