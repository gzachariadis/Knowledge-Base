# <i class="hgi-stroke hgi-lock-key"></i> Passkeys

Passkeys are a newer, more secure way to log in to services without relying on passwords. The [FIDO Alliance](https://fidoalliance.org/), responsible for the standard, considers it the next step towards a passwordless future. An improvement to the current system; or is it?

Unlike the traditional passwords, passkeys are generated using **public-key asymmetric cryptography**. In order to prove your identity, instead of typing in a password, you now use your private-key to authenticate your identity to a platform.

In this article, we’ll explain all about

- what passkeys are
- why they are considered an evolution to passwords
- what are we to gain by switching

and a lot more...

## Definition

A passkey is a type of digital key used to log into websites and apps, passkeys use your device (like your phone or computer) to securely authenticate your identity. 

## How does it work?

When you set up a passkey, your device stores a special pair of keys 

- public key (shared with the website or app)
- private key (kept secret on your device)

When you log in, the website or app sends a request, and your device uses the private key to confirm it's really you. It’s more complicated than that in reality, but we are here to explain concepts, not get too much into technical specifics.

The best part about this new standard? You never have to type anything, and the private key doesn't ever leave your device, making passkeys extremely secure (when properly managed).

## Purpose

The ultimate goal is an attempt to eliminate the need for passwords entirely. Instead of storing or typing passwords, the FIDO Alliance, would like the web to switch to relying on cryptographic keys stored securely on hardware devices.

So, even if someone wants to gain access to your account, they can't **without access to your physical device**, they can't extract the private key to impersonate you.

That does make a lot of sense, since there is no password to steal, passkeys are **far less vulnerable to hacks like phishing, database breaches, or keylogging**.

## Type of Passkeys

> We are only concerned here with the consumer scenario.

### Device-Bound

Lorem Ipsum

#### Features

- Backup, Backup, Backup — Loss or wipe of a device, can result in being **locked out**. Always have a backup of your keys, many companies suggest you **buy them in pairs** for exactly this reason. In case of hardware loss/failure, you will need a recovery method to re-establish your passkeys on a new device, since **they won’t be synced between devices**.

- Separation of Access — You can have separate private keys for separate devices, independently authenticating you using each device’s own private key. This means that, in case your phone is stolen, and it had a private key associated with your Google account, it's not the only key, you can still log into your Google account from your laptop or tablet, which have their own separate private keys and deauthenticate the phone's key. 
  
- Vulnerability — Syncing your private key across devices makes it convenient to access your accounts from any device, but it also means that if one device is compromised, **all devices using that synchronized private key could be at risk**.

- Manual Setup — You will need to manually set up passkeys on each device, which can be more time-consuming and inconvenient. If you use several devices, you may end up with multiple sets of keys to manage.

- Roaming — While the private key is device-bound, **if that device can come into proximity and prove presence**, for example with NFC or Bluetooth, the private key can still be accessed, now you have *“syncing”* between devices, because the private key never leaves the device, but the authenticator module, can *"roam"* &nbsp;between devices. 

### Cloud Syncing

Passkeys, by default, **are unique to each service, and device**. Having said that, they can be **synced and backed up across devices**, preferably through a **Password Manager** or by an encrypted end-to-end **Cloud Service Provider**. 

The syncing of private keys, typically, happens through encrypted cloud services like iCloud Keychain (for Apple devices) or Google Passwords (for Android/Chrome devices). These services securely sync private keys across your devices, allowing you to login to your accounts using the **same private-key on multiple devices.**

When you set up a passkey on a device, like your phone, the private key is usually stored securely on that device. In this case, it's **stored on the cloud**. Your cloud becomes this private vault, where your private-keys are stored and securely synced/transferred to your other devices ensuring you can authenticate/prove account-ownership on any device associated with your cloud account.

#### Features 

- Encryption — Make sure the private key is always encrypted during syncing, which means it cannot be read or intercepted by anyone; even the service providers (like Apple or Google). Only your devices can decrypt and use the private key to authenticate.

- Cloud Based — Your private keys are stored on service provider servers, this could result in you being susceptible to theft or hack.

- Ecosystem Bound — Stewardship has to be with someone, if you use iCloud for syncing passkeys, you won’t be able to use it on an Android device. That means, if you are not dependent on a specific ecosystem, you should rely on a third-party for stewardship, something like a Password Manager.

- Shareability — You share one private key between devices, making you susceptible to being locked out. The same way, having a device-bound private-keys does.

#### Comparison

Device-bound passkeys are fundamentally extremely secure, if managed properly, and that's an if that considers some thought, considering as of writing this, it's still expensive and requires you to take ownership and stewardship of your data.

On the other hand, essentially, what cloud-based does, is it takes away the burden of management from you, trading it in, for compromised privacy and security, you trust your cloud service provider to keep your private-keys away from hackers and always provide maintenance and access to your data, without locking you out. 

The choice is yours.

### Security

One of my first questions, researching this was *“How is this an improvement if I am already using a randomly generated non-identifiable password on each site?”* Let’s answer it…

TLDR; and without getting into technical details, **passkeys are as secure as the method you store them**. 

Additionally, **the same as passwords, your private keys, can be stolen, just less easily...**

The main advantage of passkeys is that they are extremely hard to steal. With traditional passwords, if a hacker gets access to a password database, they can use these passwords to break into accounts. With passkeys, even if someone steals your data from a company server, they still have to get access to the private key stored on your device, which is what actually grants access.

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

The way passkeys are implemented, for example on a phone, all you need is a security module installed on the device called WebAuthN, then when a passkey is initiated or triggered, the website, can communicate through Javascript with your phone and pop-up a phone login action, provided it’s successful, the device and website exchange information on a challenge, the phone completes, website verifies it’s successful and you are logged in.

The Authenticator component of the Operating System and the Client (usually a Browser performing authentication) require presence and proximity, there are different ways that prove this connection, but basically the private key, can’t be not stored on-device or transmitted to a device via network; bluetooth, NFC or usb, only go so far.

Because it combines multiple protocols and security features, like having to unlock your keychain / authentication module on your operating system, whether by a biometric or pin, having an intent gesture, like touching a hardware key or actively initiating a login procedure. The authentication process  is much more secure.

The aim is to be as hardware-based as possible.

#### Security Features

- Phishing Protection — Passkeys stop phishing attacks. Since you don’t manually type anything to log in, a hacker can’t trick you into entering your password on a fake website. The authentication process relies on your device, so it only works on the legitimate website or app.

- Data Breach Protection — Your private-keys is not susceptible to data breach on the website/app’s server, meaning it can't be stolen to impersonate you, just like a password can.

- Increased Security — RSA cryptographic keys are so long, it’s a virtual impossibility to break them, compared to weak passwords that can be easily cracked.

#### Privacy Concerns

##### Biometrics

I am not aware of any devices, aka, mobile phones that send biometric data to providers, like Google or another manufacturer. I wholeheartedly believe they are stored on the device, if that's not the case, I would for sure advise against using biometrics to unlock your passkeys, just like I wouldn't store them in the cloud.

But how do biometrics work? Biometrics, are an **indirect method**, for sending your pin or password to the device itself, that's what actually triggers the unlock function. In other words, instead of typing your pin, the fingerprint reader, checks what it has *"on-file"* within local storage, and compares it with what feedback is pressed upon the reader and when those match, the pin is transmitted to the device causing an unlock trigger. **The final action is always a pin code that triggers the unlock, not biometrics.** 

The biometrics are not what you think too, it’s **not a picture of your face or your fingerprint**. The typical fingerprint tech is a Capacitance Grid, the capacitors get charged and emit a value, multiple of those values together form a pattern that’s unique to your finger.

Therefore, you don’t need to be afraid of biometrics on phones and laptops, and you are **not forced to use biometrics to unlock your passkeys**, but in case you are, it’s fine as long as they are **stored on device**.

##### Bluetooth BLE

BLE doesn’t require pairing, just requires some application listening. 
	
No specific threats to this point.

Doesn’t use the internet, communication is out of band.

##### Cross Device Tracking

Passkeys associate a private-key with a device. Provided that, this device is your phone, it is now **permanently and directly used to confirm your identity to the platform**. That in turn means, having multiple identities under the same platform, on the same phone is out of the question.

Passkeys force a much more clear attachment to the device than passwords, therefore, they can be used for tracking or better put, associating a unique phone to a person.

Although, you should be aware that passkeys, are not prohibitive to the use of other devices and not a phone. Hardware keys, for example, can also be used, making the phone just an in-between device and not the one associated directly with the platform.

##### Cross-Domain Tracking & Phishing Attacks

The passkey has an integrated private key, a derivative private/public key associated based on the domain identity (Relying Party); it’s **unique** so it **does not leak cross-domain identity and tracking.**

As should your passwords be, **unique to each website**. The system doesn’t fundamentally change, except from the fact, your private keys are stored securely on your device. The passkeys, still correspond to individual services and are used to authorize your login, just like your passwords used to do. Fundamentally, you exchange your secure random passwords database for a database with secure private keys. 

Similarly, while password managers can help fill-in login details automatically, they **don't fully protect against phishing attacks**. Phishing protection can still be bypassed by very convincing fake sites, because it's a form of link-based protection; you or your password manager's auto-fill feature, can be tricked into navigating onto a fake website, and filling in your details, effectively sharing them with a malicious actor.

Passkeys are much more resistant to phishing attacks because they **don’t rely on typing or submitting anything at all**. Instead, the authentication process uses your device to assign a verification challenge to your private key, which can't be prompted by a malicious site.

##### Credential Storage

A backup of your private key could potentially be stored by the platform of your phone provider, if you choose to initiate it through a phone, aka Google Cloud or iCloud.

Should you be worried about Google storing your private key? Probably not, if it’s end-to-end encrypted, think of it like Google requiring your master password on a password manager, to view your passwords, which they don’t have.

You should be aware that, when opting to initiate passkey creation, through platform providers (Google,Apple,Microsoft), they will be able to see what platform the private-key is being associated with. 

That means, theoretically at least, **platform providers are able to associate you with platforms and your accounts under those platforms**. Not sure, I would want any of those to know which platforms I have accounts with.

## Passwords vs Passkeys - What’s the Difference?

Under the current infrastructure, most accounts use a traditional password, which is something **you create**, usually a combination of letters, numbers, and symbols, that you use to log into your accounts. 

Hopefully, most of us at least, use a password manager and apply the recommended principles. Righttttttt? Well, some people do, most don’t, and that's exactly who the enemy of the current system is — **people**.

**People left to their own devices, will come up with memorable, non-secure, reusable passwords. Who do we know? Data Breaches!**; there have been tons of them.

Which brings me to my second enemy walkthrough, **companies**. Some companies are terrible at managing passwords, they store them with no encryption, have faulty infrastructure, get hacked etc. etc. so, can you really trust them? Think about how many accounts you have, trust a few companies, but all? Right...

Currently, both sides of the current infrastructure cause problems, so what do we have to gain by switching? Well, let’s look at the differences...

#### Advantages - against Passwords

- Reusability — Passkeys are not reusable.

- Security — Passwords are crackable, especially weak ones.

- Knowledge — We have no access to see how our passwords are stored on a website’s/company’s servers, whether they are encrypted, properly secured etc.

- Convenience — No retyping passwords and having to change them all the time.

- Enforced Security — Passwords can be stolen in a myriad of ways, even through the mere action of copying them in the clipboard.

- Data Breach Protection — In case of a data breach, passkeys are stored only on your device, so the service/company doesn't store a password to be stolen.

- No Reliance on Human Cognition — You don't have to remember your password.

#### Cons - against Passwords

- Hackable — Same as passwords, passkeys are only as safe as the place you store them.

- Encryption — Not encrypted by default, they can be stolen just like if you write your plain text passwords somewhere.

- Limited Availability — Currently, only a few providers support them. There’s a few resources right [here]() and [here.](https://github.com/bitwarden/passkeys-index )

- Non-Compartmentalized (by Default) — Can be stored in the same device as your password & 2FA codes.

### Can an Online Account truly be Passkey-Only Access?

In theory, **yes**, an online account can be passkey-only access—but in practice? Unluckily. There’s always the need for backup methods, either for account recovery or for setting up new devices. These fallback options are in place to ensure you don’t get locked out.

Another note to consider, is this, almost all major services still require an email address, or a phone number. Why is that so? Couldn’t they all be based on a username? Absolutely, but **why deny the obvious benefit of identifying you through an email address or phone number**. And here's why there isn’t a pass-key only access to most online accounts, most services are KYC (Know Your Customer).

That's not the only reason though, people are a factor too; we lose keys, don't backup data, switch phones, forget passwords; that means passkey access-only account
will almost-never be an option, by major platforms at least, because there will always be a need for account recovery.

### Notes

Passkeys basically do the authentication on the device, because in order to decrypt or in most cases use your private key to authenticate, you have to unlock the device, provide a pin or something.

- Private Keys can be stored on a password manager.

- Passkeys to be initiated on Bitwarden require the browser extension.

- Passkeys can be synced using Bitwarden

- Passkeys can be exported.

- You can store passkeys both to your Bitwarden Vault and to your Hardware Key

- Passkeys don’t expire.

- What happens if a passkey is stolen or compromised?

- Where to store my passkeys? Hardware or Software?

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
