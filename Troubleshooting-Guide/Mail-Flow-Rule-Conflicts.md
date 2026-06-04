## Overview
Problem Description
Emails behave unexpectedly due to multiple or conflicting transport (mail flow) rules, such as:
- Disclaimers not appearing
- External tagging missing
- Emails incorrectly redirected or blocked
- HR or security rules overriding each other

## Causes
- Multiple rules applying to the same message
- Rule priority (order) misconfiguration
- Stop processing more rules enabled
- Overlapping conditions (e.g., sender + recipient + subject)
- Incorrect scope (Inside/Outside organization mismatch)

## Troubleshooting Steps
Step 1: I check Mail Flow Rules Order
      Open Exchange Admin Center:
Exchange Admin Center
Navigate to Mail Flow → Rules
Review rule priority (top = highest priority)

👉 Higher rules execute first.

Step 2: Review Rule Conditions
Check for overlapping conditions:
External sender rules
Domain-based conditions
Recipient-specific rules


Step 3: Check “Stop Processing More Rules”
If enabled, lower rules will not run
Disable if multiple rules must apply

Step 4: Use Message Trace
- Go to Exchange Admin Center
- Navigate to Mail Flow → Message Trace
- Track affected email
- Review which rule was applied

# Resolution Best Practices
- Keep rule design simple and modular
- Avoid overlapping conditions
- Document rule hierarchy
- Use consistent naming conventions
