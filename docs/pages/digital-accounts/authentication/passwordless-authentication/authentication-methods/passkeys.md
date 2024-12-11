---
alias: wuthering-heights
---

# <i class="hgi-stroke hgi-lock-key"></i> Passkeys

<br> 

##### #Definition

> A **passkey** is a type of **"digital key"** used to log into websites and apps, passkeys use your device, like your phone or computer, to securely authenticate your identity. 

## Introduction

Passkeys are a newer standard, aimed at allowing passwordless login to services. The [FIDO Alliance](https://fidoalliance.org/), responsible for the standard, considers it the next step towards a passwordless future.

The ultimate goal of the standard, is an attempt to <u>eliminate the need for passwords</u> *ENTIRELY*. 

Instead of coming up with, storing and typing/filling in passwords, the [FIDO Alliance](https://fidoalliance.org/), would like the Web to switch on relying to **cryptographic keys** stored securely on hardware devices.

So,  <span>theoretically, at least, </span> if someone wants access to your account, they can't impersonate you - *without the* **private-key** - which is securely stored on a device <u>you *physically possess*</u>.

The main point you should keep in mind is that, since there is *no password to steal*, **Passkeys** are *far less vulnerable* to attacks like **phishing**, **database breaches**, or **keylogging**.

## How does it work?

Unlike the traditional passwords, passkeys are algorithmically generated using **public-key asymmetric cryptography**. This means that, in order to prove ownership of an account, instead of typing in a **password**, you can now use a **private-key** to authenticate your identity to a platform.

In order for **Passkeys** to work, your device stores a special pair of keys a **public key**, shared with the website or app and a **private-key**, which is kept *secret* <u>on your device</u>.

When you attempt a login, the website or app sends a request, and your device uses the **private-key** to confirm account ownership. 

In reality, it's must more complicated than that, but we are here to explain concepts, not get too much into technical specifics.

The best part about this new standard for both users and companies alike, is **getting rid of passwords**. More on that later...

<span>What are you to gain as a user? you might ask...</span> Well, this new standard eliminates the need for *memorizing or typing passwords*, and considering the **private-key** *never leaves* your device, **Passkeys** are *extremely secure*, under the *proper management*.

## Passkey Types

### Device-Bound

Device-bound **Passkeys** are a type of **security-key** that are *tied directly to a specific device*, such as your phone, laptop, or **hardware-key** device. 

This is the default, when it comes to **Passkeys** as their purpose is to associate a specific device to a specific account.

When you use a **device-bound Passkey**, your device stores a unique key that is <u>*only stored*</u> on that device. This means that for an intruder to successfully login into your account, he/she would require physical access to your specific device to authorize entry.

??? danger "Pay Attention!"

    It's worth noting that while the private-key is device-bound, the **Authenticator Module**, can be triggered <span>"remotely"</span>, under certain conditions; 
    
    One being, two devices coming into **proximity** and **proving presence**, for example with *[NFC](../../../../glossary/near-field-communication.md)* or *Bluetooth*, the private-key can still be accessed <u>*"essentially remotely"*</u>. This creates a form of **“syncing”** between devices, because the private-key never leaves the *actual hardware device*, but the *Authenticator Module*, can <span>"roam"</span> and authenticate between devices. 


**Device-bound Passkeys**, on multiple devices can be *time-consuming*, especially, the first-time around; requiring you to go through each of the services that support it, and sit through the process of associating them with your account. Think of it, a bit like, changing your password to all your accounts, all at once; 

<span>...just a pain in the ass!</span>


##### Usage Tips

- <span>Backup, Backup, Backup</span> — **Device-bound Passkeys**, are susceptible to *hardware loss* or *hardware failure*, both of those, can result in being <u>*temporarily or permanently locked*</u> out of accounts. Many companies advise purchasing **hardware-keys** <u>*in pairs*</u>, to avoid exactly this scenario.

- <span>Separation of Access</span> — The average user possesses more than one device, be it a laptop and a phone, multiple mobile phones or even multiple physical **hardware-keys**, that means that, you can initiate *separate* **Passkeys** for <u>*each of your devices*</u>; a way to <u>*independently*</u> *authenticate*. On top of that, it's an unofficial form of backup, making you less likely to be locked out of your accounts.

### Cloud Syncing

Passkeys, by default, are *unique to each service and device*. Having said that, they can be *synced* and *backed up across devices*, preferably through a **Password Manager** or by an end-to-end encrypted **Cloud Service Provider**. 

The syncing of **Passkeys**, or in reality, **private-keys**, typically, happens through **cloud services** like *iCloud Keychain* (for Apple devices) or *Google Passwords* (for Android/Chrome devices). These services securely sync private-keys across your devices, allowing you to login to your accounts using the *same* **Passkey** *on multiple devices*.

That's worth explaining a bit more...

When you set up a passkey on a device, like your phone, for example, the **private-key** is typically *stored on device*. Under this scenario, it's **stored on the cloud**. 

Your cloud storage becomes this **private vault**, where your **private-keys** are stored and securely *synced*, or better put, *accessed* by your devices ensuring you can prove account-ownership via <u>*ANY*</u> *device* that has access to your cloud account. Careful of that last part, that doesn't mean only your devices.

##### Usage Tips

- <span>Encryption</span> — Make sure the **Passkey** <u>*always remains encrypted*</u>, especially during syncing, which means it cannot be accessed or intercepted; especially when using service providers, like Apple or Google. I can't stress this enough, <u>*only your devices should be able to decrypt your private-key.*</u>

- <span>Stewardship</span> — Remember, **private-keys** are <u>as secure, as the place you store them</u>; under this scenario, *the service provider servers*. This means, that, you take *responsibility* and *assign stewardship* upon the service provider, to prevent your **private-keys** against threats like *unauthorized access*, *theft*, *hacking* or *data loss*, just to name a few.

- <span>Third Party Reliance</span> — Stewardship has to be with someone, if you use *iCloud* for syncing **Passkeys**, you won’t be able to use it on an *Android* device, you are <u>*eco-system bound*</u> to use *Apple* devices. You can always *bypass this problem*, by assigning stewardship to a *third-party* like a **Password Manager**, but at the end of the day, the stewardship has to be relied-upon someone.

- <span>Vulnerability</span> — While syncing your private-key across devices offers convenience, giving you the freedom to access your accounts from any device, it also exposes all your devices to risk, if one is *compromised*, all of the devices using that synchronized **private-key** <u>*could be at risk*</u>. This situation can lead in you, quite possibly, being <u>*locked out*</u> of your accounts.
  
- <span>Conflictions</span> — Under this scenario, you decide to opt for sharing <u>*ONE*</u> **private-key** between devices. This means that, if anything, you *reduced security compared to* **Device-bound Passkeys**, and ended up switching your **threat-factors** from *hardware related* ones, like *theft*, *hardware loss* or *physical damage* to software-related like *hacking*, *online identity theft* or simply being locked out of your cloud service provider's account.

##### Conclusion

**Device-bound Passkeys** are *inherently secure*, <u><span>provided they’re properly managed</span></u>. However, this security comes with its own set of challenges—most notably, the *high cost of hardware keys* and *shouldering the responsibility of stewardship* over your data.

On the other hand, **Cloud-based Passkeys** *shift the burden of management away from you*. By entrusting a **cloud service provider** to store and protect your **private-keys**, you gain the *convenience of remote access*. However, this <span>painfully realistic trade-off</span> comes with a *compromise in privacy and security*, as you must <u>*trust*</u> your service provider to safeguard your keys from hackers and ensure you’re never locked out of your own data.

Ultimately, the choice between **Device-bound Passkeys** and **Cloud-based Passkeys** depends on your priorities — whether you value maximum security and control at the cost of some manual-work and potentially associated costs or prefer the convenience of cloud stewardship at the cost of some privacy. The decision is yours to make, and it’s important to weigh the pros and cons based on <u>*what matters most to you*</u>.

## Security

One of my first questions, researching this was <span>"How is this an improvement if I am already using a randomly generated non-identifiable password on each site?”</span>

TLDR; and without getting into technical details, I said it before, I will say it again <u>**Passkeys** *are as inherently as secure as the method you store them*</u>. Additionally, the same as **passwords**, your **private-keys**, *can be stolen*, <span>just less easily...</span>

#### Passwords vs Passkeys 

<span>First things first, let's compare **Passwords** to **Passkeys**...</span> 

Under the current infrastructure, most accounts use a traditional **password**, which is something *you create*, you come up with it, or use a **random password generator**, and you utilize that to login to your accounts. 

Hopefully, most of us, at least, use a **Password Manager** or another secure method and apply the *recommended* principles. <span>Righttttttt?</span> 

Well, some people do, <u>*most don’t*</u>, and that's exactly who the <span>"enemy"</span> of the current system is — <u>*people*</u>.

> People left to their own devices, will come up with memorable, *non-secure*, reusable passwords. 

Who do we know? **Data Breaches**, which brings us to our second enemy, <u>*companies*</u>. 

Some companies are *terrible* at managing passwords, they store them with no encryption, have faulty infrastructure, get hacked all the time...<span>so, can you really trust them?</span> Think about how many online accounts you have, <span>trust a few? Sure, but do you *FULLY* trust every company you ever had an account with? Didn't think so...</span>

As you can see, currently, both sides of the current infrastructure cause problems, <span>so what do we have to gain by switching?</span>

Well, let's take a closer look...

##### Advantages

- <span>Zero Reusability</span> — Compared to **Passwords**, **Passkeys** are <u>*not reusable*</u>, they can't be stolen and re-used on different websites.
  
- <span>Inherent Security</span> — Compared to *weak passwords* that can be <u>*easily cracked*</u>, **RSA** cryptographic keys are sooooo long, it’s a *virtual impossibility to break them*.

- <span>Freedom</span> — We have no access to see how our **Passwords** are stored on a company’s servers, with **Passkeys** you are given control over how you want to store your **private-keys**.

- <span>Convenience</span> — *No retyping* **Passwords**, coming up with new ones and having to change them all the time.

- <span>Enforced Security</span> — **Passwords** can be stolen in a myriad of ways, even through the mere action of copying them in the clipboard, **Passkeys** are <u>*inherently more secure*</u> by design.

- <span>Data Breach Protection</span> — Your **private-keys** are <u>*not susceptible*</u> to theft through a **data breach** on the website/app’s server, meaning they can't be stolen. The server only stores your **public key**, which is essentially useless by itself, to an attacker trying to impersonate you to gain access to your account.

- <span>Expiration Date</span> —  Compared to **Passwords**, **Passkeys** <u>*don’t expire*</u>, you won't need to change them regularly.

- <span>No Reliance on Human Cognition</span> — That's semi-fair point, you don't have to memorize your **Passkey**, but securing it might include a **pass-code**, **PIN** or **Password** that you might need to memorize.

- <span>Phishing Protection</span> — Passkeys stop **phishing attacks**. Since you don’t manually type anything to log in, a hacker can’t trick you into entering your **Password** on a fake website. The authentication process relies on your device, so it <u>*ONLY*</u> works on the legitimate website or app.

##### Disadvantages

- <span>Hackable</span> — Same as **Passwords**, **Passkeys** are only as safe as the place you store them.

- <span>Limited Availability</span> — Currently, lacking[^1] the universal support **Passwords** enjoy.

- <span>Non-Compartmentalized (by Default)</span> — Potentially stored in the same device, software solution as your **Passwords** & [Two-Factor Authentication]() codes.

#### Privacy Concerns

This section is focused solely on the *consumer scenario* and does not address any *business*, *professional*, or other *use cases*. The information provided is tailored to **individual consumer interests** and may not be applicable or suitable for you. 

Proceed with this in mind, as the advice and insights are specific to consumer-oriented concerns.

<br>

###### Biometrics

Biometrics handle authentication directly on your device. To use a **Passkey** stored on device, you need to provide your *unlock PIN* or to *decrypt* your **private-key** using a biometric sensor.

As far as I know, laptops, but more importantly, phones <u>*don't send biometric data to manufacturers*</u>. I strongly believe that the biometric data associated with *device unlock authentication* are *stored locally on device* (both in the case of laptops and phones). 

In other cases, it may be sent to the cloud or stored on servers for processing, in that case, I would advise against using biometrics to unlock your passkeys, because some biometric systems may be integrated with third-party services. If you use a service that shares biometric data across platforms (e.g., social media facial recognition, or payment systems), it can expose your data to additional privacy risks.

###### But how do biometrics work?

Biometrics are an **"indirect method"** of unlocking your device; instead of typing in your PIN or password, a fingerprint reader checks your biometric data against what’s stored locally on the device. When the fingerprint matches the stored data, it triggers the device to unlock. Ultimately, while **the biometric data is used for verification**, the device **unlocks based on a PIN** or other authentication mechanism, **not the biometric data itself**; biometrics are only used as a mechanism to verify the owner's presence and intention to unlock the phone.

###### Common Misconception

Since we are on the topic of biometrics; Biometrics, don't "exactly" work how you might think they do — they **don't work based on pictures of your face or your fingerprint**. The typical fingerprint technology uses a concept called *"capacitance grid"*. When touched, these capacitors, gets charged and emit a value based on pressure and pattern. The combination of all these values creates a unique pattern that corresponds to your fingerprint. This combination of values is stored on device and compared to against what's being put against the reader; therefore used to authenticate you.

###### Conclusion

Therefore, you don’t need to be afraid of biometrics on phones and laptops, and you are **not forced to use biometrics to unlock your passkeys**, but in case you are, my take, it’s fine as long as they are **stored on device**.

###### Bluetooth BLE

Bluetooth Low Energy (BLE) is a wireless communication technology designed for short-range, low-power data transmission. It is a variant of the traditional Bluetooth technology, most notably, *Bluetooth Low Energy (BLE)* allows devices to "advertise" themselves and be discovered by others without establishing a full connection, which helps conserve power.

One notable privacy concern with *Bluetooth Low Energy (BLE)* is exactly that last point, it **doesn't necessarily require pairing between devices**. Instead, it only needs an application to be listening for communication to be achieved. This means that, in some cases, devices can communicate with each other **without a formal connection**, potentially allowing unauthorized devices to listen in. 

While *Bluetooth Low Energy (BLE)* communication is done *"out of band"* (meaning it doesn't rely on the internet), it still opens the door for local interception or tracking if not properly secured. However, when actively considering the security and privacy risks, *Bluetooth Low Energy (BLE)* itself doesn’t introduce specific threats; the absence of an internet connection means that **communication is almost insusceptible to remote attacks or vulnerabilities** and the main risks, arises from the possibility of unauthorized access if **the application or device isn't properly secured**. 

###### [Cross Device Tracking](../../../../glossary/cross-device-tracking.md)

Cross-device tracking, usually refers, to the practice of linking a user’s activities across multiple devices. This often involves using unique identifiers, such as cookies or device IDs, and that's exactly the point many people fear when it comes to passkey storage.

Passkeys **associate a private key to a device**, such as your phone, which is then used to authenticate your **identity** with a platform. Even when, being used only for authentication purposes, once a passkey is stored on a device, that device is closely tied to your identity on the associated platform.

As a result, this makes almost impossible, to have multiple *"identities"* associated with the same platform on a single device, as each passkey is typically unique to each device-platform connection and tied to a specific user, allowing a platform to potentially track usage or associate activities committed by multiple accounts under a single device, to one specific user.

A proposed solution to this problem? [Hardware Keys](). Since passkey storage is not restricted to just smartphones or laptops, other devices, in this case hardware security keys, can also be used to store passkeys. 

In this case, the phone would act as an intermediary device, not directly tied to the platform, but rather enabling authentication across the device that actually stores the passkey.

Because hardware keys are separate physical devices, they do not directly tie a user to a specific phone or device, offering a higher level of privacy. When using a hardware key, even if a platform recognizes the key, it cannot uniquely associate it with a particular phone, which reduces the potential for tracking.

###### Multiple Accounts under the same Platform

Under this scenario, you could create separate user accounts within the same platform and use a unique passkey for each account; by using different passkeys for different accounts, you can prevent them from being linked to each other. 

Preferably, you would use hardware security keys for this purpose, the advantage of using hardware keys is that they provide an added layer of security, allowing you to keep each identity separate, by avoiding cross device tracking. Although, be careful, this process can prove extremely expensive, because it requires having separate physical hardware devices (aka hardware keys) for each one of your accounts to a platform. Ultimately, it's only proposed for platforms that you truly require a separate *"identity"*, not associated with your natural one.

###### Cross-Domain Tracking

A passkey depends an integrated private-key, a derivative private/public key associated with each domain identity (Relying Party); it’s **unique**, so by design **does not leak cross-domain identity and tracking**. As should your passwords be, **unique to each website**. 

The system doesn’t fundamentally change, the passkeys, just like individual passwords, still correspond to individual services and are used to validate account ownership. Fundamentally, you exchange your secure random passwords database for a database with secure private-keys. 


Passkeys are much more resistant to phishing attacks because they **don’t rely on typing or submitting anything at all**. Instead, the authentication process uses your device to assign a verification challenge to your private-key, which can't be prompted by a malicious site.

###### Phishing Attacks

While password managers can help fill-in login details automatically, they **don't fully protect against phishing attacks**. Phishing protection can still be bypassed by very convincing fake sites. You or your password manager's auto-fill feature, can be tricked into navigating onto a fake website, and filling in your details, effectively sharing them with a malicious actor.


###### Credential Storage

A backup of your private-key could potentially be stored by the platform of your phone provider (**Google Cloud** or **iCloud**) but only when you choose to initiate it through a phone.

Should you be worried about Google storing your private-key? Probably not; provided, it’s end-to-end encrypted.

In case you are not familiar with end-to-end encryption, it's a bit like Google requiring your master password on a password manager, to view your passwords, which they don’t have.

When opting to initiate passkey creation, through platform providers (Google, Apple, Microsoft), **they will be able to see what platform the private-key is being associated with**. 

That means, theoretically at least, **platform providers are able to associate you with platforms and your accounts under those platforms**. Not sure, I would want any of those to know which platforms I have accounts with.

## Frequently Asked Questions

##### - Passkey-Only Access Account

Can an account truly be passkey-only access? In theory, **yes**, an online account can be **passkey-only** access — but **in practice? Unluckily.** There’s always the need for backup methods, either for account recovery or for setting up new devices. These fallback options are in place to ensure you don’t get locked out.

Another note to consider, is this, almost all major services still require an email address, or a phone number. Why is that so? Couldn’t they all be based on a username? Absolutely, but why deny the obvious benefit of **identifying you through an email address or phone number**. And here's why there isn’t a pass-key only access to most online accounts, most services are *KYC (Know Your Customer)*.

That's not the only reason though, people are a factor too; we lose keys, don't backup data, switch phones, forget passwords; that means passkey access-only account will almost-never be an option, by major platforms at least, because there will always be a need for account recovery.

##### - Storing Passkeys under a Password Manager

Lorem Ipsum

- Passkeys to be initiated on Bitwarden require the browser extension.

- Passkeys can be synced using Bitwarden

- Passkeys can be exported.

- You can store passkeys both to your Bitwarden Vault and to your Hardware Key

##### - Stolen or compromised Passkey

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

[^1]: Here's a couple lists to check compatibility and support right [here]() and [here.](https://github.com/bitwarden/passkeys-index)

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
