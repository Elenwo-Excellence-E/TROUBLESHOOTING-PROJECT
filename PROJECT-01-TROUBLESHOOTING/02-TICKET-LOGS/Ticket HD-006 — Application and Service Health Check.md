Ticket HD-006 — Application and Service Health Check

Environment: Ubuntu Server VM (zp-web01)
Category: Application / Service Support
Priority: P2 — Moderate
Status: Investigation complete; service checks successful

Reported issue

A simulated user reported that an application on the server was not behaving as expected and requested an investigation of its service status and logs.

Troubleshooting performed

Checked Apache service status using systemctl status apache2 --no-pager.

Reviewed recent service journal entries using sudo journalctl -u apache2 -n 20 --no-pager.

Inspected Apache's error log using sudo tail -n 20 /var/log/apache2/error.log.

Validated Apache configuration using sudo apache2ctl configtest.

Tested local HTTP responses using curl against 127.0.0.1 and 127.0.1.1.

Findings

Apache was active and running and enabled at boot.

The visible log entries mainly showed startup and graceful-restart activity.

Apache emitted a warning about not reliably determining its fully qualified domain name.

The configuration test returned Syntax OK.

Both local HTTP requests returned HTTP/1.1 200 OK.

Resolution and conclusion

The checks did not reproduce an Apache service outage. The server returned successful local HTTP responses and the configuration syntax was valid. The hostname warning was documented for potential future review; no configuration changes were made.

The cause of the simulated application complaint remains undetermined because the affected application and the user's exact symptoms were not specified.

Skills demonstrated

Linux service-status checks, journal and error-log review, configuration validation, HTTP response testing, and evidence-based incident documentation.

Scope: Controlled home-lab exercise; no production systems involved.