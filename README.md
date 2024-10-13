Video Streaming Microservice Platform

This project is a microservice-based video streaming platform built using Node.js. The platform supports uploading, storing, and streaming media files efficiently. We utilize Multer, a middleware for handling multipart/form-data, which is primarily used for uploading files in Node.js applications.
Features

    Media Upload: Allows users to upload video and other media files.
    Media Storage: Uses Multer to handle file uploads and storage.
    Video Streaming: Supports streaming of media files in real-time.
    Microservice Architecture: Modular design for better scalability and maintainability.

Technologies

    Node.js: Backend runtime environment for building the server.
    Express.js: Framework for building web applications and APIs.
    Multer: Middleware for handling file uploads.
    Stream API: Utilized for streaming media to users.

Getting Started
Prerequisites

Before you can run this application, make sure you have:

    Node.js installed
    npm or yarn installed

Installation

    Clone the repository:

    bash

git clone https://github.com/your-repo/video-streaming-platform.git
cd video-streaming-platform

Install dependencies:

bash

npm install
# or
yarn install

Create a .env file in the root directory and add your environment variables:

bash

    PORT=3000
    STORAGE_PATH=./uploads

Running the Application

To start the application:

bash

npm start
# or
yarn start

This will launch the server at http://localhost:3000.
API Endpoints

    POST /upload: Endpoint for uploading media files.

        Example:

        bash

    curl -F 'file=@/path/to/your/video.mp4' http://localhost:3000/upload

GET /video/
: Endpoint for streaming the video.

    Example:

    bash

        http://localhost:3000/video/sample.mp4

Folder Structure

plaintext

├── controllers
│   └── videoController.js   # Handles video upload and streaming logic
├── routes
│   └── videoRoutes.js       # Defines routes for video operations
├── uploads                  # Default folder where uploaded media is stored
├── app.js                   # Main server file
