# Overview
This Mail flow rules (also known as Transport Rules) in Exchange Online allow harford property administrators to control how email messages are processed within the organization. These rules is used to apply disclaimers, redirect messages, block specific attachment types, and identify emails originating from external senders.

Rule 1: Add an External Email Disclaimer
## Objective
Append a disclaimer to all outbound emails sent outside the organization.

# Navigation Path
Exchange Admin Center
└── Mail Flow
    └── Rules
        └── Add a Rule
Steps
- Sign in to the Exchange Admin Center.
- Navigate to Mail Flow → Rules.
- Click Add a Rule (+).
- Select Create a new rule.
- Configure:
Name: External Email Disclaimer
Apply this rule if: The recipient is located Outside the organization
Do the following: Apply a disclaimer to the message
Disclaimer text,
If the sender is outside the organization harfordpm@christtech.co.uk
- Set audit severity level to 'High' and Delete the message without notifying the recipient or sender
- Except if
Is received from a member of group 'harfordpm@christtech.co.uk'

Click Save.
# Outcome
All outbound emails will automatically include the organization's disclaimer.

Rule2: Redirect HR Emails
    Objective:
    Redirect emails sent to the HR mailbox to a designated HR administrator or shared mailbox.
# Navigating Path
Exchange Admin Center
└── Mail Flow
    └── Rules
        └── Add a Rule
Steps
Navigate to Mail Flow → Rules.
Click Add a Rule (+) → Create a new rule.
Configure:
Name: HR Email Redirect
Apply this rule if: Recipient is external to harfordpm@christtech.co.uk
Do the following: Redirect the message to harfordpm@christtech.co.uk
Click Save.

# Outcome
All emails sent to the HR mailbox are automatically redirected to the designated HR contact.

Rule3:Block Dangerous Attachments
      Objective:
      To prevent users from sending or receiving potentially harmful file types.

# Navigating Path
Exchange Admin Center
└── Mail Flow
    └── Rules
        └── Add a Rule
Steps
Navigate to Mail Flow → Rules.
Click Add a Rule (+) → Create a new rule.
Configure:
Name: Block Dangerous Attachments
Apply this rule if: Any attachment has these file extensions
Add the following extensions:
.exe
.bat
.vbs
Click Finish

# Outcome
Messages containing executable or script-based attachments are blocked before delivery.
