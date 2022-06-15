## Authentication Cheat Sheet

* Introduction
Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

## Authentication General Guidelines

User IDs
Make sure your usernames/user IDs are case-insensitive. User 'smith' and user 'Smith' should be the same user. Usernames should also be unique. For high-security applications, usernames could be assigned and secret instead of user-defined public data.

Email address as a User ID
For information on validating email addresses, please visit the input validation cheatsheet email discussion.

## Authentication Solution and Sensitive Accounts

Do NOT allow login with sensitive accounts (i.e. accounts that can be used internally within the solution such as to a back-end / middle-ware / DB) to any front-end user-interface
Do NOT use the same authentication solution (e.g. IDP / AD) used internally for unsecured access (e.g. public access / DMZ)

## Implement Proper Password Strength Controls

A key concern when using passwords for authentication is password strength. A "strong" password policy makes it difficult or even improbable for one to guess the password through either manual or automated means. The following characteristics define a strong password:

. Password Length

* Minimum length of the passwords should be enforced by the application. Passwords shorter than 8 characters are considered to be weak (NIST SP800-63B).
* Maximum password length should not be set too low, as it will prevent users from creating passphrases. A common maximum length is 64 characters due to limitations in certain hashing algorithms, as discussed in the Password Storage Cheat Sheet. It is important to set a maximum password length to prevent long password Denial of Service attacks.
. Do not silently truncate passwords. The Password Storage Cheat Sheet provides further guidance on how to handle passwords that are longer than the maximum length.
. Allow usage of all characters including unicode and whitespace. There should be no password composition rules limiting the type of characters permitted.
Ensure credential rotation when a password leak, or at the time of compromise identification.
. Include password strength meter to help users create a more complex password and block common and previously breached passwords
 * zxcvbn library can be used for this purpose. (Note that this library is no longer maintained)
 * Pwned Passwords is a service where passwords can be checked against previously breached passwords. You can host it yourself or use API.

 ## Store Passwords in a Secure Fashion
It is critical for an application to store a password using the right cryptographic technique. Please see Password Storage Cheat Sheet for details on this feature.

## Change Password Feature
When developing change password feature, ensure to have:

User is authenticated with active session.
Current password verification. This is to ensure that it's the legitimate user who is changing the password. The abuse case is this: a legitimate user is using public computer to login. This user forgets to logout. Then another user is using this public computer. If we don't verify current password, this another user able to change the password.

## Authentication and Error Messages
Incorrectly implemented error messages in the case of authentication functionality can be used for the purposes of user ID and password enumeration. An application should respond (both HTTP and HTML) in a generic manner.