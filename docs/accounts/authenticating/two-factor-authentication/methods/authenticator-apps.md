Authenticator Apps, be it **Aegis**, **Google Authenticator**, **Authy** or something else, all fundamentally use the same **open-standard** protocols.

- **TOTP (Time-based One-Time Passwords)** 
  
- **HOTP (HMAC-based One-Time Passwords)** 

Although these protocols themselves are open-standard, not all implementations are created equally, implementations usually vary based on the application. More on that later, for now, all you need to know about **TOTP** and **2FA (Two-Factor Authentication) Applications**, is that they’re based on a <u>**Shared Secret**</u> called the *“seed”*, *“constant factor”* or *“hash”*.

When you set up **TOTP**, the service (the website or application) shares with you a **secret code**. This is something only you and the service **are supposed to know** and it’s assumed **(hint!)** only you and the website have access to this. Because both you and the service have access to this shared secret, that’s why we call it, **Symmetric Encryption**. 

This shared secret is used by the app to generate a new one-time password that changes every 30 seconds because it’s based on the current time. Remember? Time-based One Time Passwords (TOTP). From now on, everytime you try to log in, you use your Authentication App. The secret code aka “seed” you configured for the service is then used to create one of these one-time passwords and thus, verify you are the owner of the account. 

Easy…Right?

### Things to take note on

Most Authenticator Applications, are susceptible to all or some of the following scenarios 

- switching phone
- changing phone number
- phone factory reset
- theft of your device
- phishing
- hacking
- malware

And a lot more ... 

All of these can force you to lose access to your accounts or suffer a security breach, so if you choose to go this route, **backups are fundamental**.

Most services still don’t allow for hardware key protocols like FIDO2 or FIDO U2F, so in case you choose or have to go this route, here’s some tips for some popular options to help you navigate this space…

### Aegis

Platform - Android

Features

- Password protected vault (avoid biometrics if possible, especially if you unlock your phone with those)
- Backup*
- Open-Source Software
- Separate passwords for backup & export*
- Tokens are hidden by default
- Auto-lock
- Categories
- Works offline
- Actively Maintained
- Allows inspection of your seeds (very important!)
- Remote panic trigger deleting vault.
- Local Storage (not cloud-based) *

Aegis offers to create a (preferably) encrypted backup of your seeds, you can do that manually, or have it be generated for you when changes are made to the vault (usually, the trigger is a new service being added). In any case, be that you manually have to remember to generate this encrypted backup and store it safely on another device for safekeeping, or one is generated for you on an interval and you just have to remember to transfer it to this other device, the application won’t do everything automatically for you. Some manual work is always required, as should it, and you are responsible for it.

Will require a separate password for encrypting-decrypting a backup.

Although it allows it to be synced to the cloud in an encrypted form using Android backup function. I have never used that, so you have to research that on your own.

### Authy 

Platform - Universal Support 

Features 

- Cloud Based

Authy uses your phone number as your way to login into your **CLOUD-BASED** (sorry for shouting!) **TOTP** codes. What happens if you switch phone and phone number at the same time? Guessed right? <u>**You locked out!**</u>

On that note, please **DO NOT** use applications like **Authy**, **Duo** or **Symantec VIP**, which 

- Don’t allow you to view and export your *"seed"* after the fact; effectively locking you into their ecosystem.

- Store your *"seed"* in the cloud. The *"seed"* is supposed to be something **YOU** have; not the company server.

- Requires a phone number or other identifiable information to authenticate your account.

- Form partnerships to offer exclusive service, on the back of open standards.

- Store codes in the cloud with no end-to-end encryption for your *"seed"*.

### OTP Auth - iOS

Features

- Encrypted Cloud Sync (through iCloud)
- Biometric Lock
- Works offline
- Local Backups
- Made by independent developer
- Separate password for backups

As far as I know, this is a decent option. So, [here’s a link](https://apps.apple.com/us/app/otp-auth/id659877384) to it.
