# Track-n-Trash

**Track-n-Trash** is an IoT-powered, computer vision-based system aimed at keeping cities clean by efficiently detecting trash overflow in bins. The system uses machine learning to identify overflowing trash and notifies the relevant authorities with the bin's timestamp and geolocation, ensuring timely waste management.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

Track-n-Trash automates waste management using real-time monitoring of bins. By leveraging computer vision and IoT devices, the system detects when trash bins are full and sends notifications to the responsible authorities. This reduces the manual inspection burden and helps maintain cleanliness in public areas.

Key components of the system include:
- ML model for trash detection
- Notification system for authorities
- IoT device integration with geolocation tagging
- An AI chatbot for user interaction
- Event tracking for cleanliness drives

## Features

- **Automatic Trash Detection**: Uses machine learning to detect overflowing trash in bins through real-time image analysis.
- **Geolocation & Timestamps**: Sends bin location and time data with each trash overflow notification.
- **Real-time Notifications**: Alerts authorities to ensure timely trash collection.
- **Ecology-Based AI Chatbot**: Assists users with trash-related queries and helps them navigate the system.
- **Community Engagement**: Encourages users to participate in cleanliness drives with eco-points and redeemable coupons.
- **Interactive Map**: Allows users to call for trash pickup services and view nearby cleanliness events.

## Tech Stack

- **Machine Learning & Computer Vision**: Python, OpenCV
- **Cloud Storage**: AWS S3 (for storing trash bin images)
- **IoT**: Devices for capturing and sending bin images
- **Backend**: python, socket.io, node, express, mongodb
- **Deployment**: AWS, Render and Vercel
- **Frontend**: ReactJS, NextJS, ShadcnUI
- **API**: Google Maps API, NotificationsAPI and Gemini

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/devrihan/WasteWatch.git
   cd WasteWatch
   ```

2. **Backend Setup**
   - Install dependencies:
     ```bash
     cd backend
     npm install  # or pip install
     ```
   - Configure environment variables for AWS S3, MongoDB, Twilio, etc.
   - Run the backend server:
     ```bash
     npm start
     ```

3. **Frontend Setup**
   - Install dependencies:
     ```bash
     cd frontend
     npm install
     ```
   - Run the frontend:
     ```bash
     npm start
     ```

4. **IoT Device Setup**
   - Deploy IoT devices on trash bins with cameras capturing images periodically.
   - Set up image uploading to AWS S3 via the IoT device's firmware.
   - Ensure the IoT devices are connected to the backend for status updates.

5. **ML Model**
   - Ensure the ML model for detecting trash overflow is trained using OpenCV.
   - Integrate the model into the backend, so the images from AWS S3 are analyzed.
   - Notify authorities once the trash threshold is crossed.

6. **Database Setup**
   - Configure MongoDB to store trash bin statuses, user points, event details, and chatbot data.

7. **Notifications**
   - Set up Twilio or any push notification service to alert authorities when bins are full.


## Usage

- **Trash Monitoring**: IoT-enabled bins continuously send images to the backend for trash level analysis.
- **Trash Overflow Detection**: When the system detects overflow, it triggers a notification containing the bin's location and timestamp.
- **User Engagement**: Users can interact with the AI chatbot to learn about nearby cleanliness drives or report trash issues.
- **Incentive System**: Users earn eco-points for participating in cleanliness drives, which can be redeemed for coupons.

## Contributions

Contributions to the project are welcome! Feel free to submit pull requests or report any issues.

## License

Distributed under the MIT License. See `LICENSE` for more information.
