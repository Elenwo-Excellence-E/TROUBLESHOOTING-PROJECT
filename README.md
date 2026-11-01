**IT Troubleshooting & Ticket Management**

Project IT Help Desk / Technical Support Portfolio

**Overview**

A hands-on home-lab project demonstrating a structured approach to troubleshooting, incident documentation, service verification, and recovery using virtual machines.

The project covers six simulated help-desk tickets, from network connectivity and account recovery to Linux storage analysis and web-server diagnostics.

**Objectives**

•Practise systematic, evidence-based troubleshooting.

•Develop familiarity with Linux administration and networking tools.

•Verify system and service behaviour before making changes.

•Document incident findings, recovery steps, and limitations.

•Maintain supporting evidence and recovery safeguards.

**Lab Environment**

Windows 11 host

Oracle VirtualBox

Ubuntu Server

Kali Linux

Apache HTTP Server

**Tools and Commands**

•Network diagnostics

ping, nslookup, ip, Test-NetConnection

•Linux account recovery

Recovery mode, root shell, account verification

•Network configuration

ip addr, ip route

•Service diagnostics

systemctl, ss, curl

•Storage analysis

df, du

•Logs and configuration

journalctl, tail, apache2ctl configtest

**Incident Register**

**HD-001**

Internet connectivity investigation

Reported problem not reproduced during tests

**HD-002**

Ubuntu password recovery

Access restored and verified

**HD-003**

Network interface recovery

Connectivity restored and tested

**HD-004**

Web service availability

HTTP 200 OK confirmed from server and Kali client

**HD-005**

Disk space investigation

No immediate storage-capacity emergency indicated

**HD-006**

Application and service health

Apache running; configuration valid; HTTP 200 OK

**Troubleshooting Approach**

Each ticket follows a consistent workflow:

I. Record the reported symptoms.

II. Gather system and diagnostic evidence.

III. Test the relevant network, service, or storage component.

IV. Compare the results against expected behaviour.

V. Apply corrective action only where justified.

VI. Verify recovery and document the outcome.

VII. Record unresolved questions and limitations.

**Evidence and Documentation**

01-Evidence/ — Ticket-specific screenshots and diagnostic evidence.

02-Ticket-Logs/ — Incident records and troubleshooting notes.

03-Final-Report/ — Detailed project report.

The project also includes a documented Ubuntu baseline and a VirtualBox recovery snapshot.

**Key Learning Outcomes**

Troubleshooting network connectivity and DNS resolution.

Recovering access to a Linux account in a lab environment.

Inspecting network interfaces and routing tables.

Verifying HTTP availability from a separate client.

Checking disk capacity, inode usage, and directory sizes.

Reviewing service logs and validating Apache configuration.

Recording evidence without assuming an unverified root cause.

**Scope and Limitations**

This project was completed in a controlled home lab using virtual machines. It is not production IT support experience.

Where tests succeeded but the reported issue could not be reproduced, the ticket records that limitation instead of claiming an unverified fix.

Career Relevance

This project demonstrates practical learning relevant to entry-level IT Help Desk, Technical Support, and IT Support Analyst positions. It complements formal cybersecurity training with hands-on troubleshooting and documentation practice.
