## Overview
Problem Description
After assigning permissions Full Access changes do not take effect immediately.
- Admin cannot open mailbox immediately
- Send As permission not working
- Access works intermittently

## Causes Discovered
- Azure AD replication delay
- Exchange Online directory sync latency
- Client-side caching (Outlook)
- Token refresh not completed
  
## Troubleshooting Steps
Step 1: Verify Permission Assignment
Run or check:

Get-MailboxPermission john.taderi@christtech.co.uk

Step 2: Wait for Propagation
Typical delays:
15 minutes – 1 hour (normal)
Up to 24 hours (rare cases)

Step 3: Force Outlook Token Refresh
Ask user to:
-Sign out and sign back in
- Restart Outlook
- Clear cached credentials
  
Step 4: Recheck Permissions
Confirm again after propagation window.

## Resolution Best Practices I took
- Allow time for replication
- Always verify via Exchange Admin Center + PowerShell
- Document change timestamp for tracking
