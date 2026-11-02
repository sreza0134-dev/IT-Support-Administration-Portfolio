# Helpdesk Tickets 006 to 010

Practice tickets. All names and details are fictional.

## INC-006: Access to the marketing shared drive
- Date: 2026-10-12
- Priority: Low
- Impact: One user, can still do most of their work
- Category: Access request
- Issue: A new team member needs access to the marketing shared drive.
- Steps taken: Confirmed name, employee ID, and team. Asked the manager to approve the access. Added the user to the marketing security group with read and edit rights. Noted the date, approver, and reason in the ticket.
- Resolution: User can open and edit files on the drive.
- Time to resolve: 15 minutes
- Follow-up: None.

## INC-007: Suspicious email reported
- Date: 2026-10-13
- Priority: High
- Impact: Possible risk to the whole company
- Category: Security
- Issue: A user received an email saying the account will be closed unless they click a link and sign in.
- Steps taken: Told the user not to click or reply. Checked the sender address and link: both looked fake. Checked whether other users got the same email and whether anyone clicked. One other user received it and did not click. Removed the email from all mailboxes and blocked the sender.
- Resolution: No account affected. Email removed and sender blocked.
- Time to resolve: 40 minutes
- Follow-up: Reminded the team how to spot phishing and to report it.

## INC-008: Websites won't load
- Date: 2026-10-14
- Priority: Medium
- Impact: One user, cannot use the web
- Category: Network
- Issue: Websites show an error, but the Wi-Fi icon shows connected.
- Steps taken: Checked the IP address: normal. Pinged 8.8.8.8: works. Pinged google.com: fails. Looked at the DNS servers: an old address that no longer exists. Confirmed with nslookup.
- Resolution: Set DNS to automatic and flushed the DNS cache. Websites load.
- Time to resolve: 20 minutes
- Follow-up: Checked two other laptops for the same old setting.

## INC-009: Phone blocked from work email
- Date: 2026-10-15
- Priority: Medium
- Impact: One user, no email on the phone
- Category: Device compliance (Intune)
- Issue: Email on the iPhone is blocked and the device shows as not compliant.
- Steps taken: Found the device in Intune. The per-setting status showed the passcode requirement failed. The user had turned off the passcode.
- Resolution: User set a passcode that follows the policy. The device synced and showed Compliant. Email access came back.
- Time to resolve: 15 minutes
- Follow-up: Reminded the user of the device requirements.

## INC-010: Employee leaving the company
- Date: 2026-10-16
- Priority: Medium
- Impact: One account, security and license
- Category: Offboarding
- Issue: An employee's last day is today, and their access needs to be closed.
- Steps taken: Got the request from HR in writing. Blocked sign-in and reset the password. Removed the user from security groups. Saved their files for the manager. Collected the laptop and phone, and removed the phone from Intune. Removed the license to free it for the next hire.
- Resolution: Access closed and the license is free again.
- Time to resolve: 45 minutes
- Follow-up: Added the date and steps to the ticket for the record.
