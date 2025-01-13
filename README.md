# Sync Code: Real-Time Collaborative Code Editor

## Introduction

Tired of sending code snippets back and forth, struggling to debug and collaborate with your team? **Sync Code** is here to revolutionize your coding experience! This intuitive collaborative code editor empowers developers and teams to work seamlessly in real time, no matter where they are. With Sync Code, you can code, debug, and ship faster—together.

---

## Features

- **Real-Time Collaboration**: Multiple users can join a room and edit code together with changes reflected instantly.
- **Room Management**:  
  - Copy button to easily copy the room ID.  
  - Leave button to exit a room.  
  - Users can rejoin the same room to continue editing.
  - User joining/leaving is reflected in real time.
- **Customizable Experience**: Syntax highlighting for different programming languages and customizable themes.
- **Docker Support**: Easy setup and deployment using Docker.

---

## Prerequisites

### Running via Docker
- **Docker**: v25.0.4  
- **Docker Compose**: v1.29.2  

### Running Locally
- **Node.js**: v20.11.1  
- **npm**: v10.2.4  
- **pm2**: v5.3.1 (Install globally using `npm i -g pm2`)  
- **nvm**: v0.39.7 (Optional for managing Node.js versions; refer to the [official documentation](https://github.com/nvm-sh/nvm) for installation.)

---

## Tech Stack

- **Frontend**: React.js, CodeMirror, React-Toastify  
- **Backend**: Node.js, Express.js  
- **Real-Time Communication**: Socket.io  

---

## Installation

### Running via Docker Image (Highly Recommended)

1. **Install Docker** on your machine.
2. Pull the image from Docker Hub:  
   ```bash
   docker pull mohitur/code-editor
   ```
3. Run the Docker container:  
   ```bash
   docker run -p 8000:8000 -p 3000:3000 -p 5000:5000 mohitur/code-editor
   ```
4. Open your browser and navigate to [http://localhost:3000](http://localhost:3000).
5. Create a new room by clicking the **Create New Room** button and entering a username.
6. Copy the room ID using the **Copy ROOM ID** button.
7. To join as another user:
   - Open a different browser, browser window, or incognito tab.
   - Navigate to [http://localhost:3000](http://localhost:3000).
   - Enter the same room ID to join.
8. Enjoy real-time collaboration by editing code across multiple instances.

**Note**: If you're using Docker in WSL2/Linux, prefix the commands with `sudo`.

---

### Running via Custom Docker Image

1. Install Docker on your machine.
2. Clone the project repository:  
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```
3. Update the `.env` file in the root directory with appropriate values.
4. Modify the `docker-compose.yml` file to replace `<your-username>`.
5. Build and run the Docker container:  
   ```bash
   docker-compose up -d
   ```
6. Open [http://localhost:3000](http://localhost:3000) in your browser.
7. Follow steps 5–7 from the **Running via Docker Image** section to create and join a room.

---

### Running Locally

1. Clone the repository and navigate to the project directory:  
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```
2. Install dependencies:  
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory and copy the content from `example.env`. Add the required credentials.
4. Start the React app:  
   ```bash
   npm start
   ```
5. In a separate terminal, start the server:  
   ```bash
   npm run server:dev
   ```
   Alternatively, use `pm2`:  
   ```bash
   pm2 start server.js
   ```
6. Open [http://localhost:3000](http://localhost:3000) in your browser.
7. Follow steps 4–7 from the **Running via Docker Image** section to create and join a room.

---

## Notes

- **Real-Time Sync**: Open the same room in multiple browsers or browser windows to see the real-time collaboration.
- **Docker**: For WSL2/Linux, remember to prefix Docker commands with `sudo`.

---

