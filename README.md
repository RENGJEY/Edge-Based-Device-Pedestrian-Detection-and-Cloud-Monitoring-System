# Edge-Based Pedestrian Detection and Cloud Monitoring System

## Introduction

This project is focused on enhancing pedestrian safety by deploying an advanced detection system on edge devices. Operating at 30 FPS, the system streams video in real-time using the RTSP protocol. The Video Storage Toolkit (VST) is employed for efficient video stream management, while Azure IoT Hub provides robust cloud-based monitoring. By combining edge computing with cloud-based oversight, this project enables seamless access and monitoring of system resources and performance, paving the way for a more secure and efficient approach to pedestrian detection and monitoring.

## Jetson Platform and OS Compatibility

This project is compatible with the NVIDIA Jetson platform. The following steps outline the installation process for DeepStream SDK, VST, and Azure IoT Hub.

### DeepStream SDK Installation

Follow the steps below to install DeepStream 6.1 on your Jetson device:

1. **Install Jetson SDK Components**
2. **Install Dependencies**
3. **Install the DeepStream SDK**
4. **Run `deepstream-app` (the reference application)**

For detailed installation instructions, refer to the [DeepStream Quickstart Guide](https://docs.nvidia.com/metropolis/deepstream/6.1/dev-guide/text/DS_Quickstart.html).

### VST(Video Storage Toolkit) Installation

The Video Storage Toolkit (VST) is essential for managing video streams. To install VST with Metropolis Microservices for Jetson:

Please refer to the [Video Storage Toolkit Quickstart Guide](https://docs.nvidia.com/moj/setup/quick-start.html).

1. **Install Platform Services**
2. **Install Application Bundle**
3. **Run IVA Application**

To start the application, navigate to the `ai_nvr` directory and run:

```bash
cd ai_nvr
```
- If on Orin AGX:
    ```bash
    sudo docker compose -f compose_agx.yaml down --remove-orphans
    ```
- If on Orin NX16:
    ```bash
    sudo docker compose -f compose_nx.yaml up -d --force-recreate
    ```
Now you should be able to test VST and use it successfully

### Azure IoT Hub Setup
To integrate Azure IoT Hub for cloud-based monitoring:

1. **Create an Azure IoT Hub**

   For detailed instructions, refer to the [Create an Azure IoT hub](https://learn.microsoft.com/en-us/azure/iot-hub/create-hub?tabs=portal).
   
2. **Create an IoT Edge Device**

   Navigate to your IoT Hub page on the Azure portal, select "IoT Edge" from the left menu, and follow the instructions to create a new IoT Edge device.
   After creation, the device will appear in the device list.
   
   ![Screenshot of the application](./example_img/1.png)

   After clicking the device ID below, you can view the detailed information of the device, such as the main connection string.

    ![Screenshot of the application](./example_img/2.png)
    p.s. You need to obtain the "primary connect string" of the device and paste it into the config file of deepstream.







