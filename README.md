# TrustEdge
TrustEdge is a binary that can run as both an **Agent**, for devices managed through [Device Trust Manager](https://www.digicert.com/device-trust-manager), and as a standalone **command line interface (CLI)** tool for performing common security tasks on a device, such as generating keys and submitting a CSR to a CA. TrustEdge is built using the DigiCert [TrustCore SDK](https://www.digicert.com/iot/trustcore-sdk).
Today, device builders need to use a number of open source tools such as OpenSSL, Paho, SCEP and other clients to perform device security tasks. TrustEdge is a *swiss army knife* for performing these common security tasks using a single, simple-to-use binary built and supported by DigiCert.
## Agent mode
TrustEdge Agent acts as the "client" to Device Trust Manager. It runs on IoT devices running a supported operating system. It is responsible for communications between the IoT device and Device Trust Manager and uses MQTT for all communications. 
More specifically, the Agent is responsible for:
- Authenticating the device with the Device Trust Manager Rendezvous Service using the device's Bootstrap Credential (e.g. x.509 certificate).
- Interfacing with secure elements on the device, such as a TPM or TEE
- Exchanging the device's Bootstrap Credential for an Operational Certificate.
- Renewing the device's Operational Certificate.
- Checking for, downloading and installing Software Updates.
- Reporting device properties (e.g. IP, MAC, etc.) to Device Trust Manager.
- Receiving a dynamically assigned MQTT broker endpoint (e.g. AWS IoT Core, Azure IoT, etc.) for sending device to cloud (D2C) and receiving cloud to device (C2D) messages.
TrustEdge includes an MQTT 3.1.1/5.0 client that IoT applications running on the device can use to communicate with any MQTT broker endpoint. The Agent also uses this MQTT client to communicate with the Device Trust Manager Rendezvous Service.
TrustEdge includes an API for applications running on the device to interact with the Agent.
In order to enable TrustEdge to work in as many environments as possible, we designed it to be generic and extensible while providing a default setup and configuration that should work for most environments. 
TrustEdge runs as a Linux daemon or Windows service, and can be ported to different RTOS platforms.
## Command Line mode
The same TrustEdge executable can also run as a standalone, command line tool (CLI) without the need for Device Trust Manager. TrustEdge CLI is useful for prototyping and accelerating an IoT pilot or proof of concept. You can use it to perform common security tasks on an IoT device such as: 
- Generating keys (RSA, ECDSA, etc.) 
- Creating a CSR
- Submitting a CSR to a CA and obtaining a certificate
- Renewing certificates
- Communicating with an MQTT broker over TLS and using x.509 authentication
## License
TrustEdge is free to download and use for non-commercial purposes, including pilots and proof of concepts. Commercial usage in a production device requires the purchase of a Device Trust Manager subscription license. See https://www.digicert.com/master-services-agreement/. 
## Documentation
TrustEdge documentation is available at https://dev.digicert.com/en/trustedge.html.
## Support
DigiCert [Device Trust Manager](https://www.digicert.com/device-trust-manager) customers with an active support contract can raise issues by creating a case with DigiCert Support at https://www.digicert.com/support/pki-support. 
Users without an active support contract can raise issues and provide feedback by creating a GitHub Issue. 