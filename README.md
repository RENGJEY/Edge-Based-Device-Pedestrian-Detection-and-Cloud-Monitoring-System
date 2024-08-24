Edge-Based Pedestrian Detection and Cloud Monitoring System
Introduction
This project is focused on enhancing pedestrian safety by deploying an advanced detection system on edge devices. Operating at 30 FPS, the system streams video in real-time using the RTSP protocol. The Video Storage Toolkit (VST) is employed for efficient video stream management, while Azure IoT Hub provides robust cloud-based monitoring. By combining edge computing with cloud-based oversight, this project enables seamless access and monitoring of system resources and performance, paving the way for a more secure and efficient approach to pedestrian detection and monitoring.

Jetson Platform and OS Compatibility
This project is compatible with the NVIDIA Jetson platform. The following steps outline the installation process for DeepStream SDK, VST, and Azure IoT Hub.

1. DeepStream SDK Installation
Follow the steps below to install DeepStream 6.1 on your Jetson device:

Install Jetson SDK Components
Install Dependencies
Install the DeepStream SDK
Run deepstream-app (the reference application)
For detailed installation instructions, refer to the DeepStream Quickstart Guide.

2. Video Storage Toolkit Installation
The Video Storage Toolkit (VST) is essential for managing video streams. To install VST with Metropolis Microservices for Jetson:

Install Platform Services
Install Application Bundle
Run IVA Application
To start the application, navigate to the ai_nvr directory and run:
# For Orin AGX
sudo docker compose -f compose_agx.yaml up -d --force-recreate

# For Orin NX16
sudo docker compose -f compose_nx.yaml up -d --force-recreate

Ensure the containers are running by using the sudo docker ps command.

For more information, visit the VST Quick Start Guide.

3. Azure IoT Hub Setup
To integrate Azure IoT Hub for cloud-based monitoring:

Create an Azure IoT Hub
Create an IoT Edge Device
Navigate to your IoT Hub page on the Azure portal, select "IoT Edge" from the left menu, and follow the instructions to create a new IoT Edge device. After creation, the device will appear in the device list.

For detailed instructions, refer to the Azure IoT Hub Creation Guide.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Contributions
Contributions are welcome! Please fork this repository and submit a pull request for any improvements or bug fixes.
