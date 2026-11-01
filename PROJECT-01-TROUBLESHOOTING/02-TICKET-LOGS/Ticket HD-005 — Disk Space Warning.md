Ticket HD-005 — Disk Space Warning

Environment: Ubuntu Server VM (zp-web01)
Category: Server / Storage Support
Priority: P2 — Moderate
Status: Investigation complete; warning not reproduced

Reported issue

A simulated user reported that the server was warning of low disk space and requested investigation before applications were affected.

Troubleshooting performed

Checked filesystem capacity using df -h.

Checked inode availability using df -i.

Measured top-level directory usage with sudo du -xhd1 /.

Inspected /var using sudo du -xhd1 /var 2>/dev/null.

Reviewed the reported usage of /var/lib, /var/cache, and /var/log.

Findings

Root filesystem /dev/sda2: approximately 9.8 GB total, 5.4 GB used, and 4.0 GB available.

Root filesystem utilization: 58%.

Inode utilization: approximately 1% in the earlier check.

/var: approximately 814 MB.

/var/lib: 359 MB.

/var/cache: 322 MB.

/var/log: 123 MB.

Resolution and conclusion

The reported low-disk-space problem was not reproduced. Available space remained approximately 4.0 GB, and inode exhaustion was not indicated. The largest identified /var subdirectory was /var/lib, followed by /var/cache and /var/log.

No files were deleted and no system configuration was changed. The cause of the simulated warning remains undetermined.

Skills demonstrated

Filesystem capacity checks, inode monitoring, Linux directory-usage analysis, evidence-based troubleshooting, and incident documentation.

Scope: Controlled home-lab simulation; no production systems involved.