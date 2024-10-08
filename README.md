# face-recognition-software

## Overview

Face Recognition Software is a .NET-based application designed to recognize and verify employees by comparing uploaded images against a stored database of employee images. This software utilizes ASP.NET Core for the backend API and ImageSharp for image processing.

## Features

- **Image Upload**: Users can upload an image for recognition.
- **Face Recognition**: Compares the uploaded image with stored images to identify the person.
- **Real-time Processing**: The system provides instant feedback on whether the person is recognized.
- **Security Alerts**: If the person is unrecognized, the system triggers a security alert.
- **CORS Support**: Configured to work seamlessly with frontend applications, such as those built with React.

## Prerequisites

- **.NET 6 SDK** or later
- **Node.js** and **npm** (for frontend if applicable)
- **Visual Studio 2022** or **Visual Studio Code**
- **ImageSharp** for image processing

## Installation

### Backend Setup

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-repository/face-recognition-software.git
    cd face-recognition-software
    ```

2. **Install Dependencies**:
    Ensure you have the required NuGet packages:
    ```bash
    dotnet restore
    ```

3. **Configure the Project**:
    Open `Program.cs` and ensure the CORS policy and `ImageProcessingService` are configured correctly.

4. **Build and Run the Backend**:
    ```bash
    dotnet build
    dotnet run
    ```

    The backend will be available at `http://localhost:5000` or `http://localhost:5217`.

### Frontend Setup (if applicable)

1. **Navigate to the Frontend Directory**:
    ```bash
    cd frontend-directory
    ```

2. **Install Dependencies**:
    ```bash
    npm install
    ```

3. **Run the Frontend**:
    ```bash
    npm start
    ```

    The frontend will be available at `http://localhost:3000`.

## Usage

### Uploading an Image

1. Open your frontend application.
2. Use the upload button to select an image from your device.
3. Click the "Check Employee" button.
4. The system will process the image and provide feedback:
   - If recognized, it will display the employee's name.
   - If unrecognized, it will alert security.

### API Endpoints

- **POST** `/api/ImageRecognition/upload`: Upload an image for recognition.
- **OPTIONS** `/api/ImageRecognition/upload`: Preflight request for CORS.