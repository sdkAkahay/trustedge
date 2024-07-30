# DigiCert<sup>®</sup> TrustEdge

> **Disclaimer:** Your use of these services, products, and software is limited to non-commercial use cases only, which includes usage for evaluation purposes prior to purchase. Commercial usage in a production environment requires the purchase of an associated entitlement.

TrustEdge is a standalone executable that can run as both an **agent** for devices managed through [DigiCert<sup>®</sup> Device Trust Manager](https://www.digicert.com/device-trust-manager) or as a standalone **command line** tool for performing common security tasks on a device, such as generating keys and submitting a certificate signing request (CSR) to a certificate authority (CA). TrustEdge is built using [DigiCert<sup>®</sup> TrustCore SDK](https://www.digicert.com/iot/trustcore-sdk).

## Agent mode

When run in agent mode, TrustEdge acts like a client to DigiCert<sup>®</sup> Device Trust Manager. It runs as daemon (Linux) or service (Windows) on an IoT device and uses MQTT for all communications between the device and Device Trust Manager.

TrustEdge agent can:

- Authenticate a device with Device Trust Manager Rendezvous Service using bootstrap credentials. For example, an x.509 certificate.
- Interface with secure hardware elements on a device, such as a TPM or TEE.
- Exchange bootstrap credentials for an operational certificate.
- Renew an operational certificate.
- Manage device updates and configurations.
- Report device properties directly to Device Trust Manager. For example, IP address, MAC address, or location.
- Receive a dynamically assigned MQTT broker endpoint for sending and receiving device-to-cloud (D2C) communications.
- Connect to other applications running on the device via an API.

## Command line mode

TrustEdge can also run as a standalone command line tool without the need for Device Trust Manager. TrustEdge command line is useful for prototyping and accelerating an IoT pilot or proof of concept. You can use it to perform common security tasks on an IoT device.

TrustEdge command line can:

- Generate keys. For example, RSA or ECDSA.
- Create a CSR.
- Submit a CSR to a CA and obtain a certificate.
- Renew a certificate.
- Communicate with an MQTT broker over TLS using x.509 authentication.

## License

TrustEdge is free to download and use for non-commercial purposes, including pilots and proof of concepts. Commercial use requires the purchase of a Device Trust Manager subscription. See [LICENSE.md](LICENSE.md)</a> for additional license information.

## Documentation

TrustEdge documentation is available at https://dev.digicert.com/en/trustedge.html.

## Support

Device Trust Manager customers with an active support contract can contact DigiCert Support at https://www.digicert.com/support/pki-support.

If you do not have an active support contract, you can provide feedback by creating an [issue](https://github.com/digicert/trustedge/issues).