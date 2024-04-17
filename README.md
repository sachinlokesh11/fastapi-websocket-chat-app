---

# Chat Application using FastAPI

This project is a simple chat application built using FastAPI, featuring both group chat and one-to-one chat functionalities.

## Features

- **Group Chat:** API endpoints for group chat functionality.
- **One-to-One Chat:** API endpoints for one-to-one chat functionality.
- **WebSocket Support:** Utilizes FastAPI's WebSocket capabilities for real-time communication.
- **Frontend Interface:** Provides a basic frontend chat view using HTML templates.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/sachinlokesh11/fastapi-websocket-chat-app.git
    cd fastapi-websocket-chat-app
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Run the FastAPI application:

    ```bash
    uvicorn main:app --reload
    ```

2. Access the application in your web browser:

    ```
    http://localhost:8000
    ```

## Project Structure

- **`main.py`:** Contains the FastAPI API endpoints for the chat application.
- **`model.py`:** Includes the FastAPI WebSocket connection manager code.
- **`templates/`:** Directory containing HTML templates for the frontend chat view.
- **`requirements.txt`:** Lists all Python dependencies. Install them using `pip install -r requirements.txt`.

## Understanding the APIs

### Group Chat

- **Endpoint:** `/{client_id}`
- **Description:** WebSocket endpoint for group chat.
- **Functionality:**
  - Connects clients to the chat room.
  - Broadcast messages to all connected clients.
  - Handles disconnections and notifies other clients.

### One-to-One Chat

- **Endpoint:** `/{client_id}/{receiver_id}`
- **Description:** WebSocket endpoint for one-to-one chat.
- **Functionality:**
  - Connects clients to a specific chat room based on client and receiver IDs.
  - Sends messages only to the intended receiver.
  - Handles disconnections and notifies the other client in the conversation.

## Special Thanks

I would like to extend my sincere thanks to the creators of the numerous resources and tutorials that have been instrumental in the development of this project. Your clear explanations, insightful guides, and generous sharing of knowledge have been invaluable in helping me navigate through the complexities of building a chat application with FastAPI. Your dedication to educating and empowering developers is deeply appreciated.

## Credits

This project was created and maintained by [Sachin](https://github.com/sachinlokesh11).

---
