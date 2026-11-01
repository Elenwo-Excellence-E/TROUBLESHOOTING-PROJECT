Ticket HD-004 — Web Service Unavailable

Environment: Ubuntu Server VM (zp-web01) and Kali Linux client
Category: Application / Web Service Support
Priority: P2 — Moderate
Status: Testing successful; original issue not reproduced

Reported issue

A simulated user reported that the server appeared online but its website could not be accessed.

Troubleshooting performed

Checked Apache service status using systemctl status apache2.

Inspected listening TCP ports and associated processes using sudo ss -lntp.

Tested local HTTP access using curl -I http://127.0.0.1.

Tested HTTP access through the server interface using curl -I http://10.10.10.10.

Tested HTTP access from Kali Linux using curl -I --max-time 5 http://10.10.10.10.

Findings

Apache was active and running.

Apache was among the processes shown in the listening-port output.

Local HTTP testing returned an HTTP OK response.

Testing through 10.10.10.10 returned HTTP 200 OK.

Kali Linux also received HTTP 200 OK from the server.

Evidence

HD-004-Apache-Service-Status.png
HD-004-Local-HTTP-Test.png
HD-004-Kali-Client-HTTP-Test.png

Resolution and conclusion

All tested access paths succeeded. The reported website-access problem could not be reproduced in this lab. No configuration changes were required, and the original cause remains undetermined.

Skills demonstrated

Linux service inspection, TCP listening-port inspection, HTTP response testing, client-side connectivity testing, evidence-based diagnosis, and incident documentation.

Scope: Simulated home-lab exercise; no production systems involved.