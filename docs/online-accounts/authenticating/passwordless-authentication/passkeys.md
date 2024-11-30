Passkeys are a newer, more secure way to log in to services without relying on passwords. The FIDO Alliance (responsible for the standard) wants you to think about it like the next iteration to a passwordless future. An improvement, if you will.

Unlike the traditional passwords, passkeys are generated using public-key asymmetric cryptography to prove your identity, making them harder for hackers to steal. 

In this blog post, we’ll explain all about, what passkeys are, why they are considered an evolution to passwords, are they really a safer alternative to passwords for keeping your accounts secure and a lot more…Let’s begin.

## Definition

A passkey is a type of digital key used to log into websites and apps, passkeys use your device (like your phone or computer) to securely authenticate your identity. 

## How though?

When you set up a passkey, your device stores a special pair of keys 

- public key (shared with the website or app)
- private key (kept secret on your device)

When you log in, the website or app sends a request, and your device uses the private key to confirm it's really you. It’s more complicated than that in reality, but we are here to explain concepts, not get into technical specifics.

The best part about this new standard? You never have to type anything, and the private key doesn't leave your device, making passkeys extremely secure (when properly managed).

## Purpose

The ultimate goal is an attempt to eliminate the need for passwords entirely. Instead of storing or typing passwords, the FIDO Alliance, would like the web to switch to relying on cryptographic keys stored securely on hardware devices. 

So, even if someone gains access to anything but your actual device, they cannot extract the private key to impersonate you; and that does make sense, since there is no password to steal, passkeys are far less vulnerable to hacks like phishing, database breaches, or keylogging.

## Type of Passkeys

- Device-bound
- Synced

### Device-Bound

#### Features

- Stored in USB, or TPM of a device. 
- Can be lost.

We are only concerned here with the consumer scenario.

- Backup, Backup, Backup — Loss or wipe of a device, can result in being locked out. Always have a backup of your keys. Otherwise, you will need a recovery method to re-establish your passkeys on a new device, since they won’t be synced.

- Separation of Access — You can have separate private keys, for separate devices, so you can still access your accounts from your other devices and independently authenticate you using each device’s own key. So, if your phone is stolen, and it had a private key synced to your Google account, you can still log into your Google account from your laptop or tablet, which have their own separate private keys. Syncing your private key across devices makes it convenient to access your accounts from any device, but it also means that if one device is compromised, all devices using that key could be at risk.

- Manual Setup — You will need to manually set up passkeys on each device, which can be more time-consuming and inconvenient. If you use several devices, you may end up with multiple sets of keys to manage.

- Roaming — While the private key is device-bound, if that device can come into proximity and prove presence, for example with NFC or Bluetooth or be plugged in and the private key can be accessed, now you have “syncing” between devices, because the private key never leaves the device, but the Authenticator module, can be roaming   between devices. 

### Synced Passkey

Passkeys should be unique to each service, not device. Passkeys can be synced and backed up across devices, preferably through a password manager or an encrypted end-to-end system. Essentially, all you need is for your private key used in passkeys to be synced across devices. 

The syncing of private keys typically happens through encrypted cloud services like iCloud Keychain (for Apple devices) or Google Passwords (for Android/Chrome devices). These services securely sync private keys across your devices, allowing you to log in to websites using the same passkey on multiple devices.

When you set up a passkey on a device (like your phone), the private key is stored securely on that device. 

When you want to access the same account from a different device, the private key can be securely synced/transferred (preferably via end-to-end encryption) to your other devices, ensuring you can authenticate on any device that is linked to your account.

#### Syncing 

- Encryption — Make sure the private key is always encrypted during syncing, which means it cannot be read or intercepted by anyone; even the service providers (like Apple or Google). Only your devices can decrypt and use the private key to authenticate.

- Cloud Based — Make sure your keys are not stored in the cloud, this could result in you being susceptible to theft.

- Ecosystem Bound — Stewardship has to be with someone, if you use iCloud for syncing passkeys, you won’t be able to use it on an Android device. That means, if you are not dependent on a specific ecosystem, you should rely on a third-part for stewardship, something like a Password Manager. But essentially, what cloud-based does, is it takes away the burden of management from you.

- Shareability — You share one private key between devices, natively in some cases based on your Operating System.

### Security

TLDR; and without getting into technical details, passkeys are as secure as the method you store them, the same as password, your private keys, can be stolen and used to authenticate you.

One of my first questions, researching this was “How is this an improvement if I am already using a randomly generated non-identifiable password on each site?” Let’s answer it…

The main advantage of passkeys is that they are extremely hard to steal. With traditional passwords, if a hacker gets access to a password database, they can use those passwords to break into accounts. With passkeys, even if someone steals your data, they can’t get the private key stored on your device, which is what actually grants access.

Relying Party

CTAP

USB

NFC

Hybrid — BLE (Bluetooth) + HTTPS

Authenticator

First Party

Examples, iOS keychain - native to device.

Third Party

Some other authenticator installed on the device Microsoft Authenticator

Passkeys also offer protection against phishing attacks. Since you don’t manually type anything to log in, a hacker can’t trick you into entering your password on a fake website. The authentication process relies on your device, so it only works on the legitimate website or app.

The way passkeys are implemented, for example on a phone, all you need is a security module installed on the device called WebAuthN, then when a passkey is initiated or triggered, the website, can communicate through Javascript with your phone and pop-up a phone login action, provided it’s successful, the device and website exchange information on a challenge, the phone completes, website verifies it’s successful and you are logged in.

The Authenticator component of the Operating System and the Client (usually a Browser performing authentication) require presence and proximity, there are different ways that prove this connection, but basically the private key, can’t be not stored on-device or transmitted to a device via network; bluetooth, NFC or usb, only go so far.
Because it combines multiple protocols and security features, like having to unlock your keychain / authentication module on your operating system, whether by a biometric or pin, having an intent gesture, like touching a hardware key or actively initiating a login procedure. The authentication process  is much more secure.
The aim is to be as hardware-based as possible.

- Biometrics

I am not aware of any devices, aka, mobile phones that send biometric data to providers, like Google or whatever manufacturer, I do believe they are stored on the device, if not, I would for sure advise against using biometrics to unlock your passkeys.

Biometrics, are used as an indirect method, to sending your pin or password for unlocking the device, to the device itself, in other ways, instead of typing it, the fingerprint reader, compares what it has in local storage, with what feedback is given on the reader and when those match, the pin is transmitted to the device for an unlock to occur. The final action is always a pin code that triggers the unlock, not biometrics. 

The pin-code on a phone is used to do that storage encryption and that is stored only on the device.

The biometrics are not used as you think too, it’s not a picture of your face or data about your fingerprint someone can download. The typical fingerprint tech is a Capacitance Grid, the capacitors get charged and emit a value, multiple of those values together form a pattern that’s unique to your finger.

You don’t need to be afraid of biometrics on phones and laptops, so far….

You are not forced to use biometrics to unlock your passkeys, but in case you are, it’s fine as long as they are stored on the device, that’s my take. 

- Bluetooth BLE

BLE doesn’t require pairing, just requires some application listening. 
	
No specific threats to this point.

Doesn’t use the internet, communication is out of band.

- Cross Device Tracking

They use the phone to confirm your identity. So multiple identities on the same platform under the same phone, won’t work because they can tie your identity to your phone. The phone identifiers are transmitted to the platform.

Passkeys force a much more clear attachment to the device than passwords, therefore, they can be used for tracking or better put, associating a unique phone to a person. 

Although you should be aware that passkeys, the standard itself, is not prohibitive to the use of other devices and not a phone. Hardware keys can also be used, making the phone just an in-between device and not the one associated directly with the platform.

- Passkey Credential Storage

By default, the backup or your private key will probably be stored by the platform of your phone provider, if you choose to initiate it through a phone, aka Google Cloud or iCloud.
There’s another option for passkey storage, and it’s Password Managers, things like 1Password and 

Bitwarden are also members of FIDO Alliance and implement passkeys.
Should you be worried about Google storing your private key? Probably not, it’s end-to-end encrypted, think of it like Google requiring your master password on a password manager, to view your passwords, which they don’t have.

Although that does sound secure, enough at least to consider me switching to potentially passkeys, we should be aware that, when storing and initiating this passkey creation, Google or Apple or Microsoft if you are using Windows, should be able to see what platform it’s associated with. Linking that to your profile. Not sure, I would want any of those to know which platforms I have accounts with.

Okay, so…

- your password is not susceptible to data breach on the website/app’s server.

- better protection against phishing attacks.

- RSA cryptographic keys are so long it’s a virtual impossibility to break passwords this way.

### Passwords vs Passkeys - What’s the Difference?

Under the current infrastructure, most accounts use a traditional password, which is something you create, usually a combination of letters, numbers, and symbols, that you use to log into your accounts. 

Hopefully, most of us at least, use a password manager. Righttttttt? Well, some people do, some don’t and that’s the face of the enemy — people. People left to their own devices, will come up with memorable, non-secure, reusable passwords. 

Who do we know? Data breaches, there have been tons of them. 

Which brings me to my second enemy walkthrough, companies. Some companies are terrible at managing passwords, they store them with no encryption, they have faulty infrastructure, they get hacked etc. etc. so, can you really trust them? Think about how many accounts you have, trust a few, but all? Right….Both sides of the current infrastructure cause problems.

Let’s look at the compassion between both sides of the aisle.

#### Pros

- Reusability — Passkeys are not reusable.

- Security — Passwords are crackable, especially weak ones.

- Knowledge — We have no access to see how our passwords are stored on a website’s/company’s servers, whether they are encrypted, properly secured etc.

- Convenience — No retyping passwords and having to change them all the time.

- Enforced  Security — Passwords can be stolen in a myriad of ways, even through the mere action of copying them in the clipboard.

- Data Breach Protection — In case of a data breach (hack), passkeys are stored only on your device, so the service doesn't store a password to be stolen.

- No Reliance on Human Cognition — The WebAuthN module takes care of the verification for you.

#### Cons

- Hackable — Same as passwords, passkeys are only as safe as the place you store them.. 

- Encryption — Not encrypted by default, they can be stolen just like if you write your plain text passwords somewhere.

- Limited Availability — They are not accepted in most places, just yet.

- P2P shareability (Software Implementation) — you can share your private key with different devices through syncing, they don’t have to be hardware bound on a single device.

- Non-Compartmentalized by Default — Can be stored in the same device as your password & 2FA codes.

<br>

Okay…Let’s look at this way, you are a security conscious consumer, you generate pseudo-random passwords, long and complicated using a password manager, you don’t reuse the same password across sites, In other words, you operate within considerably high operation security (OpSec). You even autofill your passwords using a browser extension with 2FA, so you are not able to be keylogged. What are you to gain? 

Passkeys are the next level to passwords, by proposing that you keep your “password” (in this scenario your private key) on your device and give services a public key, that’s because in case of a breach, your password doesn’t get compromised, your public key does (hint! It’s called public for a reason).

Okay, that takes care of the data breach issue, however, both of these suffer the same issues — they can be stolen if someone gets access to your account or your device.

### Supported Services

There’s a list right [here]. More and more services join the FIDO Alliance and implement Passkeys and WebAuth daily.

### Password Manager Integration

Although password managers can help fill in login details automatically, they don't fully protect against phishing attacks. While some password managers include basic phishing protection (like website URL checks), they can still be bypassed by very convincing fake sites.

In many cases, you can be tricked into navigating onto a fake website, causing the password manager to fill in your details, possibly sending your password to a malicious site. 

Passkeys are much more resistant to phishing attacks because they don’t rely on typing or submitting passwords at all. Instead, the authentication process uses your device to sign a challenge with your private key, which is unique to that website or service.

### Each service - a new unique private key? How many keys will I have to store?

The passkey has an integrated private key, a derivative private/public key based on the domain name; it’s unique so it does not leak cross-domain identity and tracking.

As should your passwords be, unique to each website, the system doesn’t change, your private keys are stored securely on your device, correspond to a different service and are used to authorize your login, just like your passwords should do. 

Fundamentally, you exchange your secure  random passwords database for a database with secure private keys. 

### Can an Online Account truly be Passkey-Only Access?

In theory, yes, an online account can be passkey-only access—but in practice? Unluckily. There’s always the need for backup methods for account recovery and setting up new devices, there are usually fallback options in place to ensure you don’t get locked out.

Another note to consider is this, almost all major services still require an email address, or a phone number. Why is that so? Couldn’t they all be based on a username? Absolutely, but why deny the obvious benefit of identifying you through an email address or phone number. And here's why there isn’t a pass-key only access to most online accounts, most services are KYC (Know Your Customer).

Well, they also ask for your account recovery. Most people lose keys, forget to backup their computer or switch phones forgetting to backup their private keys. Be that as it may, that means that an account is never passkey-only because you will always have some other way to login, even to set up a new passkey, like prompts or email or some other verification.

### Notes

Passkeys basically do the authentication on the device, because in order to decrypt or in most cases use your private key to authenticate, you have to unlock the device, provide a pin or something.

- Private Keys can be stored on a password manager.

- Passkeys to be initiated on Bitwarden require the browser extension.

- Passkeys can be synced using Bitwarden

- Passkeys can be exported.

- Device-bound vs Synchronized

- You can store passkeys both to your Bitwarden Vault and to your Hardware Key

- Passkeys don’t expire.

- What happens if a passkey is stolen or compromised?

- Where to store my passkeys? Hardware or Software?

- https://github.com/bitwarden/passkeys-index List of Services that allow passkeys

### Sources

- [What is a Passkey? by Ask Leo!](https://www.youtube.com/watch?v=6lBixL_qpro)

- [FIDO Promises a Life Without Passwords by IBM Technology](https://www.youtube.com/watch?v=lRFeuSH9t44)

- [Passwords vs. Passkeys - FIDO Bites Back! by IBM Technology](https://www.youtube.com/watch?v=9nrE4t4-IXA)

- [Understand passkeys in 4 minutes by Chrome for Developers](https://www.youtube.com/watch?v=2xdV-xut7EQ)

- [How Can Passkeys Possibly Be Safe? By Ask Leo!](https://www.youtube.com/watch?v=EA9mK3nJE1o)

- [Passkeys Vs Passwords & MFA - Weighting the Pros and Cons! By Shannon Morse](https://www.youtube.com/watch?v=rKKkF19JF2w)

- [What Are Passkeys? - Are Passwords Going EOL?! By Shannon Morse](https://www.youtube.com/watch?v=wuylMMB8CsU)

- [Passwordless Passkey Logins 2023 - Are they Safe for Privacy? by Rob Braxman Tech](https://www.youtube.com/watch?v=dpTVXCjJQyY)

- [Bitwarden and Passkeys Webcast by Bitwarden](https://www.youtube.com/watch?v=2r6NbdhThmA)

- [Store passkeys in Bitwarden by Bitwarden](https://www.youtube.com/watch?v=pfEmIk2a_Xs)

- [Passwordless Authentication: Weighing the Options by IBM Technology](https://www.youtube.com/watch?v=f6LD9sDKQq8)
