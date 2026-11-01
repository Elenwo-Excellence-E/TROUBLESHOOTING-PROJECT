Ticket HD-003 — Network Connectivity Lost in Ubuntu Server Lab

Environment: Ubuntu Server virtual machine
Hostname: zp-web01
Affected interface: enp0s3
Incident type: Network connectivity troubleshooting
Status: Resolved — lab verification successful

Incident summary

A controlled lab test temporarily disabled the enp0s3 network interface to simulate a network connectivity failure.

Troubleshooting performed

Inspected network interface status and IP configuration.

Reviewed the routing table and identified the default route.

Temporarily disabled enp0s3 to reproduce the connectivity failure.

Re-enabled enp0s3.

Verified that the interface was running and network connectivity had returned.

Successfully pinged 1.1.1.1 and punchng.com.

Findings

The successful ping to 1.1.1.1 confirmed IP connectivity. The successful ping to punchng.com additionally indicated that DNS resolution was functioning.

Resolution

Restored the network interface and verified connectivity using ping tests.

Evidence
HD-003-Network-Recovery-Verification.png

Preventive lesson

When investigating a connectivity incident, check the interface state, IP configuration, routing table, and DNS resolution systematically before making further changes.

Scope: Controlled home-lab simulation. No production systems were involved.