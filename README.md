# 💬 ChattingApplication

A simple socket-based client-server chat application written in Python. This project demonstrates basic networking concepts using TCP sockets and threading, allowing multiple clients to connect to a single server, send messages, and receive responses in real-time.

---

## 🧠 Key Features

- ✅ Multi-client support via threading
- ✅ Client name auto-assignment on connection
- ✅ Server responds to client messages with uppercase echo
- ✅ Graceful disconnection with `"CLOSE SOCKET"` command
- ✅ Real-time console logging of chat events
- ✅ Bi-directional messaging between server and clients

---

## 📁 Project Structure

```
ChattingApplication/
├── client.py   # Client-side logic (connect, send/receive, close)
├── server.py   # Server-side logic (listen, handle clients, broadcast)
├── main.py     # Entry point, launches server with input thread
└── .idea/      # IDE config folder (can be ignored)
```

---

## 🚀 How to Run

### 1. Start the Server

Open a terminal and run:

```bash
python main.py
```

The server will start listening on `localhost:56040` and wait for incoming client connections.

### 2. Start a Client

In a **new terminal window**, run:

```bash
python client.py
```

You will be prompted to enter the server IP (type `localhost` or `127.0.0.1` for local testing), then type `CONNECT` to join the server.

You can open **multiple terminals** and repeat the process to connect multiple clients concurrently.

---

## 💬 Commands

- Send any message to the server:  
  The server will echo it back in **UPPERCASE**.

- Type `CLOSE SOCKET` from the client:  
  Gracefully disconnects from the server.

- Type messages directly in the server terminal:  
  The server can broadcast to all clients as "Server: your message".

---

## 🔐 Notes

- All communication is in UTF-8 over TCP.
- Ports and host settings are hardcoded but can be modified easily.
- No GUI is implemented — this is a **pure CLI-based chat tool** for educational purposes.

---

## 📚 Educational Goals

This project is ideal for:

- Understanding Python socket programming
- Learning multi-threaded server design
- Practicing message broadcasting and real-time communication
- Experimenting with TCP/IP protocols

---

## 👨‍💻 Author

**Mahmoud Elfeel**  
🔗 [GitHub Profile](https://github.com/mahmoudelfeelig)

---

## 📖 License

This project is licensed under the [MIT License](LICENSE).
