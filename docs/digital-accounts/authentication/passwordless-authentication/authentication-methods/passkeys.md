# <i class="hgi-stroke hgi-lock-key"></i> Passkeys

<br> #Definition

> A *passkey* is a type of *"digital key"* used to log into websites and apps, passkeys use your device, like your phone or computer, to securely authenticate your identity. 

## Introduction

Passkeys are a newer, more secure way to log in to services without relying on passwords. The [FIDO Alliance](https://fidoalliance.org/), responsible for the standard, considers it the next step towards a passwordless future.

The ultimate goal is an attempt to eliminate the need for passwords entirely. Instead of storing or typing passwords, the FIDO Alliance, would like the web to switch to relying on cryptographic keys stored securely on hardware devices.

So, even if someone wants to gain access to your account, they can't **without access to your physical device**, they simply cannot access the private-key to impersonate you.

The main point you should keep in mind is that, since there is **no password to steal**, passkeys are **far less vulnerable to hacks like phishing, database breaches, or keylogging**.

## How does it work?

Unlike the traditional passwords, passkeys are algorithmically generated using **public-key asymmetric cryptography**. This means that, in order to prove ownership of an account, instead of typing in a password, you can now use a private-key to authenticate your identity to a platform.

When you set up a passkey, your device stores a special pair of keys 

- public key (shared with the website or app)
- private-key (kept secret on your device)

When you attempt a login, the website or app sends a request, and your device uses the private-key to confirm account ownership. In reality, it's must more complicated than that, but we are here to explain concepts, not get too much into technical specifics.

The best part about this new standard for both users and companies alike, is **getting rid of passwords**. On top of that, you never have to type anything, and the **private-key doesn't ever leave your device**, making passkeys **extremely secure**, under proper management.

## Passkey Types

> We are only concerned here with the consumer scenario.

### Device-Bound

Device-bound passkeys are a type of security key that are tied directly to a specific device, such as your phone, laptop, or hardware key. This is the default, when it comes to passkeys as their purpose is to associate a specific device, through the use of a private-key to a specific account.

When you use a device-bound passkey, your device stores a unique key that is only usable on that device. This means that even if someone tries to hack into your account, they would need physical access to your specific device to gain entry.

It's worth noting that while the private-key is device-bound, if that two devices can come into **proximity** and **prove presence**, for example with *[NFC](../../../../glossary/near-field-communication.md)* or *Bluetooth*, the private-key can still be accessed remotely. This creates a form of **“syncing”** between devices, because the private-key never leaves the actual hardware device, but the *authenticator module*, can **"roam"** between devices. 

Device-bound passkeys, on multiple devices can be **time-consuming** the first-time around; requiring you to go through each of the services that support it, and sit through the process of associating it with your account. Think of it, like changing your password to all your accounts, all at once.

<span>Usage Tips</span>

- <span>Backup, Backup, Backup</span> — Device bound passkeys, are susceptible to hardware loss or failure, both of those, can result in being **temporarily or permanently locked out of accounts**. Many companies advise purchasing **hardware keys in pairs**, to avoid exactly this scenario.

- <span>Separation of Access</span> — The average user possesses more than one device, be it a laptop and a phone, multiple mobile phones or physical hardware keys, that means that, you can **initiate separate private-keys for each of your devices; a way to independently authenticate**. On top of that, it's an unofficial form of backup, making you less likely to be locked out of your accounts.

### Cloud Syncing

Passkeys, by default, are **unique** to each service, and **device**. Having said that, they can be **synced and backed up across devices**, preferably through a *Password Manager* or by an end-to-end encrypted **Cloud Service Provider**. 

The syncing of private-keys, typically, happens through cloud services like **iCloud Keychain** (for Apple devices) or **Google Passwords** (for Android/Chrome devices). These services securely sync private-keys across your devices, allowing you to login to your accounts using the **same private-key on multiple devices**.

That's worth explaining a bit more, when you set up a passkey on a device, like your phone, the private-key is usually **stored on device**. In this case, it's **stored on the cloud**. Your cloud account becomes this **private vault**, where your private-keys are stored and securely synced, or better put, accessed from your devices ensuring you can authenticate/prove account-ownership on any device with access to your cloud account. Careful of that last part, that doesn't mean only your devices.

<span>Usage Tips</span>

- <span>Encryption</span> — Make sure the private-key is **always** remains **encrypted** during syncing, which means it cannot be read or intercepted by anyone; even the service providers (like Apple or Google). Only your devices should be able to decrypt your private-key.

- <span>Stewardship</span> — Remember, private-keys are as secure, as the place you store them; in this case, **the service provider servers**. This means, that, you take responsibility and **assign stewardship**, as well as, security upon the service provider, to prevent your private-keys against unauthorized access, theft, hacking or loss.

- <span>Ecosystem Bound</span> — Stewardship has to be with someone, if you use Apple's **iCloud** for syncing passkeys, you won’t be able to use it on an **Android** device, you are eco-system bound to use Apple devices. Of course, you can by-pass this problem, by assigning stewardship to a third-party like a *Password Manager*, but at the end of the way, the stewardship has to be relied-upon someone.

- <span>Vulnerability</span> — While syncing your private-key across devices offers convenience, giving you the freedom to access your accounts from any device, it also exposes all your devices to risk, **if one is compromised**, **all devices using that synchronized private-key could be at <u>risk</u>,** possibly resulting in your being locked out of your accounts.
  
- <span>Shareability</span> — You share one private-key between devices, making you susceptible to being locked out. This means that, if anything, you reduced security compared to device-bound private-keys, and ended up switching your threat-factors from hardware failure or loss to software-related like hacking, wipe of device or being locked out of your cloud account.

<span>Conclusion</span>

Device-bound passkeys are **inherently secure**, provided they’re properly managed. However, this security comes with its own set of challenges—most notably, the **high cost of hardware keys** and **shouldering the responsibility of stewardship over your data**.

On the other hand, cloud-based passkeys **shift the burden of management away from you**. By entrusting a cloud service provider to store and protect your private-keys, you gain the convenience of automated maintenance and remote access. However, this trade-off comes with a compromise in privacy and security, as you must trust your provider to safeguard your keys from hackers and ensure you’re never locked out of your own data.

Ultimately, the choice between device-bound and cloud-based passkeys depends on your priorities — whether you value maximum security and control at the cost of some manual-work and potentially associated costs or prefer the convenience of cloud management at the cost of some privacy. The decision is yours to make, and it’s important to weigh the pros and cons based on what matters most to you.

## Security

One of my first questions, researching this was “How is this an improvement if I am already using a randomly generated non-identifiable password on each site?” Let’s answer it…

TLDR; and without getting into technical details, **passkeys are as secure as the method you store them**. Additionally, **the same as passwords, your private-keys, can be stolen, just less easily...**

#### Passwords vs Passkeys 

First, let's compare passwords to passkeys...Under the current infrastructure, most accounts use a traditional password, which is something **you create**, usually a combination of letters, numbers, and symbols, that you use to log into your accounts. 

Hopefully, most of us at least, use a *Password Manager* and apply the recommended principles. **Righttttttt?** Well, some people do, **most don’t**, and that's exactly who the enemy of the current system is — **people**.

> People left to their own devices, will come up with memorable, non-secure, reusable passwords. 

Who do we know? **Data Breaches**; there have been tons of them.

Which brings us to our second enemy, **companies**. Some companies are terrible at managing passwords, they store them with no encryption, have faulty infrastructure, get hacked all the time...so, can you really trust them? Think about how many accounts you have, trust a few, yeah, but all? Didn't think so...

As you can see, currently, both sides of the current infrastructure cause problems, so what do we have to gain by switching? 

Well, take a closer look...

#### Advantages — against Passwords

- <span>Zero Reusability</span> — Passkeys are not reusable, they can't be stolen and re-used just like passwords can.
  
- <span>Inherent Security</span> — RSA cryptographic keys are so long, it’s a virtual impossibility to break them, compared to weak passwords that can be easily cracked.

- <span>Zero Knowledge Approach</span> — We have no access to see how our passwords are stored on a company’s servers, whether they are encrypted, properly secured etc.

- <span>Convenience</span> — No retyping passwords, come up with new ones and having to change them all the time.

- <span>Enforced Security</span> — Passwords can be stolen in a myriad of ways, even through the mere action of copying them in the clipboard, passkeys are inherently more secure.

- <span>Data Breach Protection</span> — Your private-keys are not susceptible to data breach on the website/app’s server, meaning it can't be stolen, the server only stores your public key, useless by itself to an attacker trying to impersonate you to gain access to your account.

- <span>Expiration Date</span> —  Compared to passwords, passkeys don’t expire, you won't need to change them regularly, because your private-keys are constant.

- <span>No Reliance on Human Cognition</span> — You don't have to remember your password.

- <span>Phishing Protection</span> — Passkeys stop phishing attacks. Since you don’t manually type anything to log in, a hacker can’t trick you into entering your password on a fake website. The authentication process relies on your device, so it only works on the legitimate website or app.

#### Disadvantages — against Passwords

- <span>Hackable</span> — Same as passwords, passkeys are only as safe as the place you store them.

- <span>Limited Availability</span> — Currently, lacking the universal support passwords enjoy. Here's a couple lists to check support right [here]() and [here.](https://github.com/bitwarden/passkeys-index )

- <span>Non-Compartmentalized (by Default)</span> — Can be stored in the same device as your passwords & 2FA codes.

## Technical Specifics  

> Caution! You can skip this part in case you are not interested in details about how these protocols work.

### WebAuthN

The way passkeys are implemented, all you need is a security module installed on the device called **WebAuthN**, then when a passkey is initiated or triggered, the website, can communicate through Javascript with your phone and pop-up a phone login action, provided it’s successful, the device and website exchange information on a challenge, the phone completes, website verifies it’s successful and you are logged in.

The Authenticator component of the Operating System and the Client (usually a Browser performing authentication) require presence and proximity, there are different ways that prove this connection, but basically the private-key, can’t be not stored on-device or transmitted to a device via network; bluetooth, [NFC](../../../../glossary/near-field-communication.md) or usb, only go so far.

Because it combines multiple protocols and security features, like having to unlock your keychain / authentication module on your operating system, whether by a biometric or pin, having an intent gesture, like touching a hardware key or actively initiating a login procedure. The authentication process  is much more secure.

The aim is to be as hardware-based as possible.

## Privacy Concerns

##### Biometrics

Passkeys handle authentication directly on your device. To use a passkey stored on device, you need to provide your unlock PIN or to decrypt your private key using the biometric sensor.

As far as I know, laptops, but more importantly, phones **don't send biometric data to manufacturers**. I strongly believe that the biometric data associated with authentication is stored locally on device (both in the case of laptops and phones). 

In case, that has changed somehow, or is not the currently the case, I would advise against using biometrics to unlock your passkeys. Under the same principle, I would advise against storing any identity documents (passport, driving license, identity card) in the cloud or sharing them with third-parties.

<span>But how do biometrics work?</span>

Biometrics are an **"indirect method"** of unlocking your device; instead of typing in your PIN or password, a fingerprint reader checks your biometric data against what’s stored locally on the device. When the fingerprint matches the stored data, it triggers the device to unlock. Ultimately, while **the biometric data is used for verification**, the device **unlocks based on a PIN** or other authentication mechanism, **not the biometric data itself**; biometrics are only used as a mechanism to verify the owner's presence and intention to unlock the phone.

<span>Common Misconception</span>

Since we are on the topic of biometrics; Biometrics, don't "exactly" work how you might think they do — they **don't work based on pictures of your face or your fingerprint**. The typical fingerprint technology uses a concept called *"capacitance grid"*. When touched, these capacitors, gets charged and emit a value based on pressure and pattern. The combination of all these values creates a unique pattern that corresponds to your fingerprint. This combination of values is stored on device and compared to against what's being put against the reader; therefore used to authenticate you.

<span> Conclusion</span>

Therefore, you don’t need to be afraid of biometrics on phones and laptops, and you are **not forced to use biometrics to unlock your passkeys**, but in case you are, my take, it’s fine as long as they are **stored on device**.

##### Bluetooth BLE

Bluetooth Low Energy (BLE) is a wireless communication technology designed for short-range, low-power data transmission. It is a variant of the traditional Bluetooth technology, most notably, *Bluetooth Low Energy (BLE)* allows devices to "advertise" themselves and be discovered by others without establishing a full connection, which helps conserve power.

One notable privacy concern with *Bluetooth Low Energy (BLE)* is exactly that last point, it **doesn't necessarily require pairing between devices**. Instead, it only needs an application to be listening for communication to be achieved. This means that, in some cases, devices can communicate with each other **without a formal connection**, potentially allowing unauthorized devices to listen in. 

While *Bluetooth Low Energy (BLE)* communication is done *"out of band"* (meaning it doesn't rely on the internet), it still opens the door for local interception or tracking if not properly secured. However, when actively considering the security and privacy risks, *Bluetooth Low Energy (BLE)* itself doesn’t introduce specific threats; the absence of an internet connection means that **communication is almost insusceptible to remote attacks or vulnerabilities** and the main risks, arises from the possibility of unauthorized access if **the application or device isn't properly secured**. 

##### [Cross Device Tracking](../../../../glossary/cross-device-tracking.md)

Cross-device tracking, usually refers, to the practice of linking a user’s activities across multiple devices. This often involves using unique identifiers, such as cookies or device IDs, and that's exactly the point many people fear when it comes to passkey storage.

Passkeys **associate a private key to a device**, such as your phone, which is then used to authenticate your **identity** with a platform. Even when, being used only for authentication purposes, once a passkey is stored on a device, that device is closely tied to your identity on the associated platform.

As a result, this makes almost impossible, to have multiple *"identities"* associated with the same platform on a single device, as each passkey is typically unique to each device-platform connection and tied to a specific user, allowing a platform to potentially track usage or associate activities committed by multiple accounts under a single device, to one specific user.

A proposed solution to this problem? [Hardware Keys](). Since passkey storage is not restricted to just smartphones or laptops, other devices, in this case hardware security keys, can also be used to store passkeys. 

In this case, the phone would act as an intermediary device, not directly tied to the platform, but rather enabling authentication across the device that actually stores the passkey.

Because hardware keys are separate physical devices, they do not directly tie a user to a specific phone or device, offering a higher level of privacy. When using a hardware key, even if a platform recognizes the key, it cannot uniquely associate it with a particular phone, which reduces the potential for tracking.

<span>How to Separate Multiple Accounts under the same Platform</span>

Under this scenario, you could create separate user accounts within the same platform and use a unique passkey for each account; by using different passkeys for different accounts, you can prevent them from being linked to each other. 

Preferably, you would use hardware security keys for this purpose, the advantage of using hardware keys is that they provide an added layer of security, allowing you to keep each identity separate, by avoiding cross device tracking. Although, be careful, this process can prove extremely expensive, because it requires having separate physical hardware devices (aka hardware keys) for each one of your accounts to a platform. Ultimately, it's only proposed for platforms that you truly require a separate *"identity"*, not associated with your natural one.

##### Cross-Domain Tracking & Phishing Attacks

The passkey has an integrated private-key, a derivative private/public key associated based on the domain identity (Relying Party); it’s **unique** so it **does not leak cross-domain identity and tracking.**

As should your passwords be, **unique to each website**. The system doesn’t fundamentally change, except from the fact, your private-keys are stored securely on your device. The passkeys, still correspond to individual services and are used to authorize your login, just like your passwords used to do. Fundamentally, you exchange your secure random passwords database for a database with secure private-keys. 

Similarly, while password managers can help fill-in login details automatically, they **don't fully protect against phishing attacks**. Phishing protection can still be bypassed by very convincing fake sites, because it's a form of link-based protection; you or your password manager's auto-fill feature, can be tricked into navigating onto a fake website, and filling in your details, effectively sharing them with a malicious actor.

Passkeys are much more resistant to phishing attacks because they **don’t rely on typing or submitting anything at all**. Instead, the authentication process uses your device to assign a verification challenge to your private-key, which can't be prompted by a malicious site.

##### Credential Storage

A backup of your private-key could potentially be stored by the platform of your phone provider, if you choose to initiate it through a phone, aka Google Cloud or iCloud.

Should you be worried about Google storing your private-key? Probably not, if it’s end-to-end encrypted, think of it like Google requiring your master password on a password manager, to view your passwords, which they don’t have.

You should be aware that, when opting to initiate passkey creation, through platform providers (Google, Apple, Microsoft), they will be able to see what platform the private-key is being associated with. 

That means, theoretically at least, **platform providers are able to associate you with platforms and your accounts under those platforms**. Not sure, I would want any of those to know which platforms I have accounts with.

## Frequently Asked Questions

###### - Passkey-Only Access Account

Can an account truly be passkey-only access? In theory, **yes**, an online account can be **passkey-only** access — but **in practice? Unluckily.** There’s always the need for backup methods, either for account recovery or for setting up new devices. These fallback options are in place to ensure you don’t get locked out.

Another note to consider, is this, almost all major services still require an email address, or a phone number. Why is that so? Couldn’t they all be based on a username? Absolutely, but why deny the obvious benefit of **identifying you through an email address or phone number**. And here's why there isn’t a pass-key only access to most online accounts, most services are *KYC (Know Your Customer)*.

That's not the only reason though, people are a factor too; we lose keys, don't backup data, switch phones, forget passwords; that means passkey access-only account will almost-never be an option, by major platforms at least, because there will always be a need for account recovery.

###### - Storing Passkeys under a *Password Manager*

Lorem Ipsum

- Passkeys to be initiated on Bitwarden require the browser extension.

- Passkeys can be synced using Bitwarden

- Passkeys can be exported.

- You can store passkeys both to your Bitwarden Vault and to your Hardware Key

###### - Stolen or compromised Passkey

Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum

## Glossary

Relying Party

CTAP

Hybrid — BLE (Bluetooth) + HTTPS

Authenticator

First Party

Examples, iOS keychain - native to device.

Third Party

Some other authenticator installed on the device Microsoft Authenticator

## Notes

- Where to store my passkeys? Hardware or Software?

## Sources

- [What is a Passkey? by Ask Leo!](https://www.youtube.com/watch?v=6lBixL_qpro)

- [FIDO Promises a Life Without Passwords by IBM Technology](https://www.youtube.com/watch?v=lRFeuSH9t44)

- [Passwords vs. Passkeys - FIDO Bites Back! by IBM Technology](https://www.youtube.com/watch?v=9nrE4t4-IXA)

- [Understand passkeys in 4 minutes by Chrome for Developers](https://www.youtube.com/watch?v=2xdV-xut7EQ)

- [How Can Passkeys Possibly Be Safe? by Ask Leo!](https://www.youtube.com/watch?v=EA9mK3nJE1o)

- [Passkeys vs Passwords & MFA - Weighting the Pros and Cons! by Shannon Morse](https://www.youtube.com/watch?v=rKKkF19JF2w)

- [What Are Passkeys? - Are Passwords Going EOL?! by Shannon Morse](https://www.youtube.com/watch?v=wuylMMB8CsU)

- [Passwordless Passkey Logins 2023 - Are they Safe for Privacy? by Rob Braxman Tech](https://www.youtube.com/watch?v=dpTVXCjJQyY)

- [Bitwarden and Passkeys Webcast by Bitwarden](https://www.youtube.com/watch?v=2r6NbdhThmA)

- [Store passkeys in Bitwarden by Bitwarden](https://www.youtube.com/watch?v=pfEmIk2a_Xs)

- [Passwordless Authentication: Weighing the Options by IBM Technology](https://www.youtube.com/watch?v=f6LD9sDKQq8)
