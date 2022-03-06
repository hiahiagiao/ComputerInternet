# homework3

### P6

> Obtain the HTTP/1.1 specification (RFC 2616). Answer the following  questions:
>
>  a. Explain the mechanism used for signaling between the client and server  to indicate that a persistent connection is being closed. Can the client, the  server, or both signal the close of a connection?
>
> b. What encryption services are provided by HTTP? 
>
> c. Can a client open three or more simultaneous connections with a given  server? 
>
> d. Either a server or a client may close a transport connection between them  if either one detects the connection has been idle for some time. Is it  possible that one side starts closing a connection while the other side is  transmitting data via this connection? Explain.

a. 

Unless the request's Connect header field contains a "close" tag, HTTP/1.1 servers can always assume that HTTP/1.1 clients want to maintain a persistent connection. If the server wants to close the connection immediately after sending a response, it should send a Connect header field with "close".  

An HTTP/1.1 client may expect to keep the connection open, but this must be based on whether the server response contains a Connect header field and whether the header field contains "close". If the client does not want to maintain the connection for more requests, it should send a Connect header field with a value of "close".  

If either client or server sends a "close" in the Connect header field, the client request will become the last request for the connection.  

Therefore, either the client or the server can send signaling to notify that the connection is closed  

b.

The HTTP protocol itself has no encryption service.

c.

No, at most two concurrent continuous connections.

d.

One side is shut down and it is impossible for the other side to transfer data over the connection.  

Therefore, the client software should be able to reopen the transport layer connection and retransmit abandoned request sequences without user interaction.  

### P12

```
`fro`m socket import *`
`serverPort = 12000`
`serverSocket = socket(AF_INET, SOCK_STREAM)`
`serverSocket.bind(("", serverPort))`
`serverSocket.listen(1)`
`print("The server is ready to receive")`
`while 1:`
    `connectSocket, addr = serverSocket.accept()`
    `sentence = connectSocket.recv(1024)`
    `print(sentence.decode())`
    connectSocket.close()`
```



