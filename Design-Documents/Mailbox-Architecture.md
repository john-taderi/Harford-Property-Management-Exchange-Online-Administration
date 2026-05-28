## Mailbox Types
Mailbox Type                                   Purpose
User Mailbox                          Individual employee email accounts
Shared Mailbox                        Departmental communication (e.g. info@ support@, accounts@)
Resource Mailbox                      Meeting rooms and equipment booking
Admin Mailbox                         IT and system administration alerts


## Naming Convention
User Mailboxes: firstname.lastnameharfordpm@christtech.co.uk
Shared Mailboxes: departmentharfordpm@christtech.co.uk
Resource Mailboxes: room-locationharfordpm@christtech.co.uk

## Architecture Flow
- Users access mailbox via Outlook (web, desktop, mobile)
- Mail routed through Exchange Online Protection (EOP)
- Policies applied before delivery (spam, rules, encryption)
- Shared mailboxes accessed via delegated permissions

## Key Design Principles
- Centralized identity using Microsoft Entra ID
- Least privilege access model
- Separation of personal and departmental mailboxes
- Cloud-first architecture (no on-prem Exchange dependency)

## Shared Mailbox Structure
Mailbox                                                Purpose                          Access Group                       
accountsharfordpm@christtech.co.uk                Finance & billing                  Accounts Team Group
supportharfordpm@christtech.co.uk                 Customer requests                  Support Team Group
infoharfordpm@christtech.co.uk                    Info communication                 Info Team Group


## Permission Model
Permission Type                                   Description                       
Full Access                                 Allows reading and managing mailbox
Send As                                     Send emails as shared mailbox identity
Send on Behalf                              Sends with user + mailbox identity


## Security Controls
- Only security groups assigned access (no individual users)
- MFA required for all users accessing shared mailboxes
- Audit logging enabled for all mailbox actions




