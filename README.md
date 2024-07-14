# Spring Boot WebSocket Live Streaming Backend

The application demonstrates how to set up a WebSocket server and create a simple interface for real-time communication.


## Use Cases for WebSockets

WebSockets enable full-duplex communication channels over a single TCP connection, making them ideal for applications that require real-time updates and low latency. Here are some common use cases:

- **Chat Applications**: WebSockets are perfect for chat applications, allowing for instant messaging between users without the need for constant polling.
- **Real-Time Gaming**: Multiplayer games require real-time data exchange, which WebSockets facilitate by providing low-latency communication.
- **Collaborative Editing**: Applications like Google Docs, where multiple users need to edit documents simultaneously, benefit from the real-time updates that WebSockets provide.
- **Live Updates**: For applications that need to push real-time updates to users, such as live sports scores or stock price changes, WebSockets are an excellent choice.
- **IoT (Internet of Things)**: Devices in an IoT ecosystem often need to communicate in real-time, which can be efficiently managed using WebSockets.

## Project Structure

```
spring-boot-websocket-live-streaming-backend/
├── .mvn/wrapper
├── src
│   ├── main
│   │   ├── java/com/alibou/websocket
│   │   │   ├── chat
│   │   │   │   ├── ChatController.java
│   │   │   │   ├── ChatMessage.java
│   │   │   │   ├── MessageType.java
│   │   │   ├── config
│   │   │   │   ├── WebSocketConfig.java
│   │   │   │   ├── WebSocketEventListener.java
│   │   │   ├── ChatApplication.java
│   │   └── resources
│   │       ├── static
│   │       └── application.properties
│   ├── test/java/com/alibou/websocket
│   │   ├── ChatApplicationTests.java
├── .gitignore
├── LICENSE
├── README.md
├── mvnw
├── mvnw.cmd
├── pom.xml
```

## Setting Up the Project

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/your-repository/spring-boot-websocket-live-streaming-backend.git
   ```

2. **Navigate to the Project Directory**:
   ```sh
   cd spring-boot-websocket-live-streaming-backend
   ```

3. **Build the Project**:
   ```sh
   ./mvnw clean install
   ```

4. **Run the Application**:
   ```sh
   ./mvnw spring-boot:run
   ```

## Project Details

### Dependencies

The project uses the following dependencies:
- `spring-boot-starter-web`: For building web applications, including RESTful applications using Spring MVC.
- `spring-boot-starter-websocket`: For building WebSocket applications.
- `spring-boot-starter-test`: For testing Spring Boot applications.
- `lombok`: For reducing boilerplate code for model objects.

### Configuration

WebSocket configuration is done in `WebSocketConfig.java`, where endpoints and message broker configurations are set up.

### Controllers and Models

- **ChatController**: Handles incoming WebSocket messages and broadcasts them to all connected clients.
- **ChatMessage**: Model class representing a chat message.
- **MessageType**: Enum representing the types of messages (CHAT, JOIN, LEAVE).

### Event Listeners

- **WebSocketEventListener**: Listens for WebSocket connect and disconnect events and logs them.

