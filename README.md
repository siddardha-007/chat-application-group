# Real-Time Chat Application (Spring Boot + WebSocket)

## Overview

This project is a real-time chat application built using Spring Boot and WebSocket (STOMP protocol).
It allows multiple users to connect, send messages, and receive updates instantly.

---

## Features

* Real-time messaging using WebSocket
* User join and leave notifications
* Broadcast messages to all connected users
* Session-based user handling
* Event-driven architecture

---

## Tech Stack

* Java
* Spring Boot
* WebSocket
* STOMP Protocol
* SockJS
* Lombok

---

## How It Works

### Flow

1. Client connects to WebSocket endpoint `/ws`
2. Client sends messages to `/app/...`
3. Server processes using `@MessageMapping`
4. Messages are broadcast to `/topic/public`
5. All subscribed clients receive updates instantly

---

## Project Structure

```id="6d4y8l"
src/main/java/com/project/chat/
│
├── config/
│   ├── WebSocketConfig.java
│   └── WebSocketEventListener.java
│
├── chat/
│   ├── ChatController.java
│   ├── ChatMessage.java
│   └── MessageType.java
```

---

## WebSocket Endpoints

| Type      | Endpoint                | Description          |
| --------- | ----------------------- | -------------------- |
| Connect   | `/ws`                   | WebSocket connection |
| Send      | `/app/chat.sendMessage` | Send message         |
| Join      | `/app/chat.addUser`     | Add user             |
| Subscribe | `/topic/public`         | Receive messages     |

---

## Running the Application

1. Clone the repository

```id="3bnmfd"
git clone https://github.com/your-username/your-repo-name.git
```

2. Navigate to project folder

```id="3c3bhu"
cd your-repo-name
```

3. Run the application

```id="o1j8l9"
mvn spring-boot:run
```

4. Open and connect to:

```id="4mbq0z"
http://localhost:8080
```

---

## Contribution

Feel free to fork, improve, and submit pull requests.
