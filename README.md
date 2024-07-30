# DigiCert<sup>®</sup> TrustEdge

> **Disclaimer:** Your use of these services, products, and software is limited to non-commercial use cases only, which includes usage for evaluation purposes prior to purchase. Commercial usage in a production environment requires the purchase of an associated entitlement.

TrustEdge is a binary that can run as both an **agent** for devices managed through [DigiCert<sup>®</sup> Device Trust Manager](https://www.digicert.com/device-trust-manager) and as a standalone **command line interface (CLI)** tool for performing common security tasks on a device, such as generating keys and submitting a CSR to a CA. TrustEdge is built using the DigiCert [TrustCore SDK](https://www.digicert.com/iot/trustcore-sdk).

## Agent mode

When run in agent mode, TrustEdge acts as the "client" to DigiCert<sup>®</sup> Device Trust Manager and runs as daemon (Linux) or service (Windows) on an IoT device. Agent mode uses MQTT for all communications between the device and Device Trust Manager.

TrustEdge agent can:

- Authenticate a device with Device Trust Manager Rendezvous Service using bootstrap credentials. For example, an x.509 certificate.
- Interface with secure elements on a device, such as a TPM or TEE.
- Exchange bootstrap credentials for an operational certificate.
- Renew an operational certificate.
- Manage device updates and configurations.
- Report device properties directly to Device Trust Manager. For example, IP address, MAC address, or location.
- Receive a dynamically assign MQTT broker endpoint for sending and receiving device-to-cloud (D2C) communications.
- Connect via an API to other applications running on the device.

## Command line mode

TrustEdge can also run as a standalone command line tool without the need for Device Trust Manager. TrustEdge command line is useful for prototyping and accelerating an IoT pilot or proof of concept. You can use it to perform common security tasks on an IoT device.

TrustEdge command line can:

- Generate keys. For example, RSA, ECDSA.
- Create a CSR.
- Submit a CSR to a CA and obtaining a certificate.
- Renewing certificates.
- Communicate with an MQTT broker over TLS using x.509 authentication.

## License

TrustEdge is free to download and use for non-commercial purposes, including pilots and proof of concepts. Commercial use requires the purchase of a Device Trust Manager subscription. See [LICENSE.md](LICENSE.md)</a>.

## Documentation

TrustEdge documentation is available at https://dev.digicert.com/en/trustedge.html.

## Support

[Device Trust Manager](https://www.digicert.com/device-trust-manager) customers with an active support contract can contact DigiCert Support at https://www.digicert.com/support/pki-support.

Users without an active support contract can provide feedback by creating an in GitHub.