# Scenario 3: User locked out of Microsoft 365

Level: Basic
Note: Practice scenario based on my Microsoft 365 lab. The details are fictional.

## Problem
A user can't sign in to Microsoft 365 (email and Teams) after getting a new phone.

## Symptoms
- The password is accepted, then the sign-in asks for approval in the Authenticator app
- The user no longer has the old phone, so they can't approve it

## Diagnostic steps
1. Confirm who is asking. Check the person's identity before changing anything on their account.
2. Check the account in the Microsoft 365 admin center. The account is active and has a license.
3. Check the sign-in logs in Entra ID. They show the sign-in stopped at the MFA step.
4. Rule out a locked account or wrong password. Neither applies.

## Root cause
The user's Authenticator app was on the old phone. With no way to approve the MFA request, the user could not sign in.

## Solution
1. Verify the user's identity
2. In Entra ID, give the user a Temporary Access Pass, or ask them to reset their sign-in methods
3. The user signs in with the pass and sets up the Authenticator app on the new phone
4. Remove the old phone from their sign-in methods
5. Ask the user to sign in normally to confirm

## Prevention
- Ask users to add a second sign-in method (for example email or a phone number)
- Give users a short guide on moving the Authenticator app to a new phone before they switch
- Turn on Self-Service Password Reset with two methods, so users can fix more problems themselves

## What I learned
Always verify identity before changing sign-in methods. A request like this can also come from someone who doesn't own the account.
