- Basic understanding of **network programming** and **sockets**.  

---
## Example Session
```
Server:
$ ./server
Server listening on /tmp/chat_socket...
On port 8080...
Client connected!
Client: Hello, Server!
You: Hi, Client!
```

```
Client:
$ ./client
Connected to server. Type 'exit' to quit.
You: Hello, Server!
Server: Hi, Client!
```

## Code Explanation
### `server.c`
-Binds the socket to port 8080 using bind().
-Listens for incoming client connections with listen().
-Accepts multiple clients and manages them using select().
-Receives messages from clients and broadcasts them to all other clients.
-Detects client disconnection and removes them from the active list.
-Closes the socket gracefully on exit.
### `client.c`
-Creates a TCP/IP socket and connects to the server at 127.0.0.1:8080.
-Sends and receives messages in real time.
-Uses send() and recv() for bi-directional communication.
-If the server disconnects, it handles the error and exits.
-When the user types exit, the connection is closed properly.
## License
This project is open-source and available under the **MIT License**.

## Authors
[saipradhamkanth(23071A3218),rithika(23071A3219),shriya(23071A3202),bhanu(23071A3204)] - Created this project for learning and demonstration purposes.
[shriya(23071A3202),bhanu(23071A3205)saipradhamkanth(23071A3218),rithika(23071A3219)] - Created this project for learning and demonstration purposes.

---
Feel free to contribute, open issues, or fork this project! 🚀
