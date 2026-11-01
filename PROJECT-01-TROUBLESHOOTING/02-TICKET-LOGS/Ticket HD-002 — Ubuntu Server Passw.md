Ticket HD-002 — Ubuntu Server Password Recovery

1. Ticket Information

Ticket ID: HD-002

Category: Account Access / Authentication

System: Ubuntu Server virtual machine

Affected account: cyberadmin

Priority: Normal (provisional; based on the available lab context)

Status: Resolved — pending final documentation review

2. User Statement

“I have forgotten the password to the Ubuntu Server.”

3. Initial Assessment

The user could not authenticate to the Ubuntu Server because the account password had been forgotten. No other administrator account was available for normal login-based recovery.

4. Troubleshooting and Recovery Performed

Accessed the Ubuntu boot recovery path.

Reached a root shell through the recovery environment.

Inspected the root filesystem mount state.

Confirmed that /dev/sda2 was mounted on / with read-write (rw) access.

Identified cyberadmin as the account to recover.

Reset the account password using root privileges.

Rebooted the Ubuntu Server.

Attempted normal login using the recovered cyberadmin account.

5. Findings

The user had lost the ability to authenticate with the previous password. Recovery access was available through the VM's root recovery environment. The root filesystem was mounted read-write, allowing the account recovery operation to proceed.

6. Resolution

The password for cyberadmin was reset using root privileges. The server was restarted after the reset.

7. Verification

The user confirmed successful normal login to Ubuntu Server using the cyberadmin account after the password reset.

8. Evidence

Root filesystem mount output: /dev/sda2 on / type ext4 (rw,relatime).

User confirmation of successful login after the password reset.

Additional screenshots or terminal logs: include only if actually captured.

9. Closure Notes

Access to the affected account was restored and normal login was verified by the user. The incident is considered resolved in the lab. No claim is made that this process was performed in a production environment.

**Post-Recovery Verification**
whoami returned cyberadmin.

hostname returned zp-web01.

id showed UID 1000 and membership in the sudo group.

sudo -v prompted for the user's password and returned to the shell prompt without a visible error.

The user had previously confirmed successful normal login after resetting the password.

Outcome: The forgotten-password incident was resolved in the Ubuntu Server lab. Normal account login was confirmed, and the observed terminal output supports successful sudo authentication.

Evidence: HD-002-Post-Recovery-Verification.png

Environment limitation: This was a recovery exercise on a personal virtual machine, not a production server.