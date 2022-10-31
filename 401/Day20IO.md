# What Socket.IO is​

#### Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server.

It is built on top of the WebSocket protocol and provides additional guarantees like fallback to HTTP long-polling or automatic reconnection.

install socket IO
[Installation steps](https://socket.io/docs/v4/server-installation/)
[API](https://socket.io/docs/v4/server-api/)
[source code](https://github.com/socketio/socket.io)

#### server

```
import { WebSocketServer } from "ws";

const server = new WebSocketServer({ port: 3000 });

server.on("connection", (socket) => {
  // send a message to the client
  socket.send(JSON.stringify({
    type: "hello from server",
    content: [ 1, "2" ]
  }));

  // receive a message from the client
  socket.on("message", (data) => {
    const packet = JSON.parse(data);

    switch (packet.type) {
      case "hello from client":
        // ...
        break;
    }
  });
});
```

#### client

```
const socket = new WebSocket("ws://localhost:3000");

socket.addEventListener("open", () => {
  // send a message to the server
  socket.send(JSON.stringify({
    type: "hello from client",
    content: [ 3, "4" ]
  }));
});

// receive a message from the server
socket.addEventListener("message", ({ data }) => {
  const packet = JSON.parse(data);

  switch (packet.type) {
    case "hello from server":
      // ...
      break;
  }
});
```

#### And here's the same example with Socket.IO:

#### Server

```
import { Server } from "socket.io";

const io = new Server(3000);

io.on("connection", (socket) => {
  // send a message to the client
  socket.emit("hello from server", 1, "2", { 3: Buffer.from([4]) });

  // receive a message from the client
  socket.on("hello from client", (...args) => {
    // ...
  });
});
```

#### client

```
import { io } from "socket.io-client";

const socket = io("ws://localhost:3000");

// send a message to the server
socket.emit("hello from client", 5, "6", { 7: Uint8Array.from([8]) });

// receive a message from the server
socket.on("hello from server", (...args) => {
  // ...
});
Copy
```

### Features

1. HTTP long-polling fallback
   The connection will fall back to HTTP long-polling in case the WebSocket connection cannot be established.

2. Automatic reconnection
   Under some particular conditions, the WebSocket connection between the server and the client can be interrupted with both sides being unaware of the broken state of the link.

3. Packet buffering
   The packets are automatically buffered when the client is disconnected, and will be sent upon reconnection.

4. Acknowledgements
   ​Socket.IO provides a convenient way to send an event and receive a response.

5. Broadcasting
   On the server-side, you can send an event to all connected clients or to a subset of clients

6. Multiplexing
   Namespaces allow you to split the logic of your application over a single shared connection. This can be useful for example if you want to create an "admin" channel that only authorized users can join.
