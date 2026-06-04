📄 Change Record: Exchange Online Initial Build
## Overview
This change records the initial setup and configuration of Exchange Online services within Microsoft 365. The build includes creation and configuration of mailboxes, resource mailboxes, mail flow rules, and foundational messaging security policies to support organizational communication requirements.

## Objectives
- Establish foundational Exchange Online environment
- Configure user, shared, room, and equipment mailboxes
- Implement mail flow (transport) rules for security and compliance
- Apply baseline email security policies
- Enable efficient resource scheduling and email management

## Mailbox Configuration
- Creation of user mailboxes
- Creation of shared mailboxes for departmental use
- Creation of room mailboxes (e.g., Boardroom)
- Creation of equipment mailboxes (e.g., Projector)

## Resource Mailboxes
- Resource Type	Name	Configuration
- Room Mailbox	Boardroom	Capacity: 12, Auto-Accept enabled
- Equipment Mailbox	Projector	Auto-Accept enabled

## Mail Flow Rules (Transport Rules)
Implemented the following rules:
Rule	Purpose
- External Email Disclaimer	Adds compliance disclaimer to external emails
- HR Redirect Rule	Redirects HR emails to designated HR mailbox
- Block Dangerous Attachments	Blocks .exe, .bat, .vbs files
- External Subject Tagging	Adds [EXTERNAL] prefix to external emails

## Mailbox Permissions & Governance
- Granted Full Access permissions to IT administrators for leaver mailboxes
- Implemented Send As permissions for shared mailboxes where required
- Documented HR and legal approval process for mailbox access

## Validation & Testing
The following tests were performed:
- Verified mailbox creation in Exchange Admin Center
- Tested room and equipment booking functionality
- Confirmed mail flow rule execution using test emails
- Validated anti-spam policy assignment to management group
- Tested Send As functionality for shared mailboxes
- Confirmed permission propagation after assignment

## Risks & Mitigation
Risk	                                    Impact	                                          Mitigation
Mail flow rule conflicts	            Email misrouting or blocking	                  Rule prioritization and testing
Permission propagation delay	        Temporary access failure	                      Allow sync time (up to 24 hours)
Misconfigured spam policy	            False positives in email filtering	            Gradual rollout and monitoring
Send As failure	                      Email identity mismatch	                        Validate permissions and restart Outlook

## Rollback Plan
- Disable or delete newly created mail flow rules if issues occur
- Remove assigned mailbox permissions if misconfigured
- Restore previous anti-spam policy settings
- Revert mailbox configurations via Exchange Admin Center

## Outcome
- Exchange Online environment successfully deployed
- Resource mailboxes operational for scheduling
- Anti-spam protections enhanced for management users
- Mailbox access governance aligned with HR and legal processes

## Change Owner
Role: Microsoft 365 Administrator
Environment: Exchange Online (Microsoft 365)
Platform: Microsoft 365 Admin Center / Exchange Admin Center

## Approval
Role	                                              Status
IT Administrator	                                 Approved
Security Team	                                     Approved
HR Department	                                     Approved (for mailbox access policies)

## Conclusion
This initial build establishes the baseline Exchange Online configuration for enterprise communication, security enforcement, and resource management. Future enhancements may include advanced DLP policies, retention labels, and automated lifecycle management.
