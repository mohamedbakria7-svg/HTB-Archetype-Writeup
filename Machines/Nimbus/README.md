# Hack The Box - Nimbus

## Machine Overview

| Field | Details |
|---|---|
| Platform | Hack The Box |
| Machine | Nimbus |
| Status | User Flag Obtained |
| Environment | Cloud / AWS |
| Documentation | English + Arabic Notes |

## 01 - Reconnaissance

Initial discovery and identification of exposed services.

## 02 - Enumeration

Investigate the web application, cloud-related functionality, and available endpoints.

## 03 - Vulnerability Analysis

### Server-Side Request Forgery (SSRF)

The investigation identified an SSRF attack path that exposed AWS instance identity information.

### Confirmed Findings

- AWS Account ID: `847219365028`
- Assumed Role: `nimbus-web-role`
- Instance ID: `i-0a1b2c3d4e5f6789a`

## 04 - Initial Access

An SQS queue was identified:

`http://floci:4566/847219365028/nimbus-jobs`

A crafted YAML message sent to the queue resulted in access to the worker container.

Confirmed shell:

`worker@d3f560a18:/app`

## 05 - Post-Exploitation

Confirmed files:

- `requirements.txt`
- `worker.py`

Further investigation is required to document the remaining privilege escalation path accurately.

## 06 - Flags

Flag values and final privilege escalation evidence will be documented after verification.

## Arabic Notes

This machine involves cloud security concepts, SSRF, AWS instance identity, SQS, and worker-container interaction.

## Disclaimer

This documentation describes authorized activity performed in the Hack The Box environment.
