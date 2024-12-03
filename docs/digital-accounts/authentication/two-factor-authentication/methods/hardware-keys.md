# Hardware Keys

Hardware Keys are physical devices that you plug into your computer or phone. Their main advantage over the competition is exactly that, they’re physical; the hacker would need to physically steal the key itself, which is technically much harder to do than stealing a text message or gaining access to an app. The security key also never exposes any secret codes to the internet that can be intercepted—it only works when you plug in and physically press a button on the device.

### How do these keys work?

Fundamentally, hardware keys use a different encryption method than the other two-methods we mentioned above.  Hardware Keys use what’s called Asymmetric Encryption. 

Under Symmetric Encryption (used by TOTP), in short, the same “key” or “secret” is used both to create and verify the password. In Asymmetric Encryption, there are two keys -- a public key and a private key. The public key can be shared openly, but the private key is always kept secret.

When you try to log in with a hardware key, it uses its private key to sign a message or request/challenge, proving that it is
the authentic key. The website or service then uses this signed key to verify the hardware signature.

### Why would I use a 2FA Hardware Key?

Pros

- SIM Swapping Resistant - When you use text messages for Two Factor Authentication (2FA), hackers can try to steal your code through a method like SIM swapping, where they trick your phone provider into giving them access to your phone number.

- No Shared Secrets - Hardware Keys use what’s called Asymmetric Encryption, among other things, like counters to produce codes that can’t be replayed, spoofed, faked etc.

- Phishing Resistance - SMS and Authenticator apps can be tricked by phishing attacks. In a phishing attack, a hacker might create a fake login page that looks exactly like the real one, and if you type in your password and 2FA code there, they can steal it. Hardware keys, don’t rely on typing in codes or checking links. When you use a key, it’s physically connected to the login process, and it only works on legitimate websites. If you try to log into a fake site, the key simply won’t authenticate, which prevents phishing attacks from being successful.

- Biometric Support - Although this can be found in some Authentication apps, having a hardware device with biometric support, is quite a plus for some people.
 
- Universal Integration - Integrates with most ecosystems, seamlessly, while most services will try to use their own verification method, like verifications prompts, SMS codes, TOTP codes etc. Hardware keys are basically the same workflow, across different ecosystems and services. Plug in and tap.

- Pin Lock - Some Authentication Applications like Google Authentication have no option to lock the App with a passcode. This means anyone with access to your phone can easily access them. Hardware keys, allow for an option to lock the key with a pin or passcode.

- Varied Applicability  - Bit of a niche, but hardware keys allow, for much more than online account authentication, for example a hardware key can be used for things like login to Linux and Windows or even a root password access request.

- Non-Syncable - The main benefit of this is that it’s stored in one place and only one place. Each key is a unique Two-Factor Authentication tool. You can’t sync it using the cloud to multiple devices or have it replicated. 

- Usability & Effortless - They can be carried with you always, they are small, require no battery ond are effortless to use. No more looking for your phone, or waiting for texts.

- Private Key Storage (Local Storage) - The private key used for authentication is stored on the physical device, not on the server (Authy I am looking at you!). This means even if a server is breached, attackers can't access your key or use it to authenticate.

- Human Presence - Most hardware keys require you to provide a “secondary” form of authentication, by touching a physical button on the key, and that’s almost impossible for a computer to replicate/spoof.

- Anonymity - Hardware Keys, once possessed do not store any information about the user directly, yes, they are connected to your online accounts, but

1. Do not require a phone number or any other personal information to function.

2. Don’t store, share or collect information about how they are used.

3. They are tied to your identity online, which you control.

Cons

- No Backup - You can’t backup the “seed” or your passcodes, like you can on TOTP, and transfer it to another device. Theoretically, that’s why they are secure, you lose the hardware key, you lose access. But, practically, solutions exist, including printing and saving your recovery codes in a safe or buying a secondary key, as a backup in case of theft or loss.

- Costly - While Text Messages and Authenticator Apps are free, security keys are a separate cost, that in some cases are extremely expensive. Plus there’s an extra cost, because usually they have to be bought in pairs, and be replaced in case of loss or theft.

- Physical Device Risk (Hardware Failure, Theft, Misplacement) - The main drawback of FIDO U2F is that you need the physical key with you. If you lose it, forget to take it with you, mismanage it, you may be locked out of your account.

- Non-Hack Proof - This will NOT make your accounts hack-proof and it’s NOT the holy grail of a solution. It’s just one of the best options we currently have. 

- Compromised Security Benefit - You should keep in mind that most accounts allow you to set up a secondary method of authentication like an email link. Which at this point, renders the security benefits, not null and void, but close to it. Because the hackers will go after this method, as it’s easier to spoof/hack. This means that in case you want the maximum benefits from this device, you should rely on it solely. Maybe with the exception of recovery codes. 

- Compatibility Chaos - Many services, including banks and investment accounts still don’t support this method. Meaning, you have to put in a lot of work, still, to find out which services support which protocols, and look at different hardware key options out there, which can cause confusion. Open-standards like FIDO2, TOTP and FIDO U2F help, but still compatibility is lacking in many respects.

- Switching Hardware - The process of moving from one key to another, requires a lot of manual work and setting up the new key into many different services, you can’t seamlessly move from one hardware to the other. Plus, it’s your responsibility to make sure the transfer is complete.

- Potentially Identifiable - Yubico as well as other hardware key manufacturers, use as part of their cryptographic signature the unique identifier of a hardware key, so if you use the key on multiple providers, you can be identified.

- Can’t be updated??? - 

<br>

Having considered the pros and cons, if you decide to buy a hardware-key, you can look at my blog-post about them here; which includes a guide on what to consider when buying one, as well, as how to form an action plan,  as well as best practices to make sure you get the most out of your hardware keys.

### Sources

- [The hardened two-factor authentication problem by Sun Knudsen](https://www.youtube.com/watch?v=01PgqzLjfuI)

- [Why most 2FA implementations are nasty and how to setup OTP Auth on iOS by Sun Knudsen](https://www.youtube.com/watch?v=7nu04NBH2Qc)

- [Why well-implemented 2FA mitigates both infosec and opsec attack vectors by Sun Knudsen](https://www.youtube.com/watch?v=VZlzPKJP4TQ)

- [Is it safe to use 2FA within a password manager? by 2FAS App](https://www.youtube.com/watch?v=PS632zXpsMc)

- [2FA Sucks by LMG Clips](https://www.youtube.com/watch?v=xhoP1dbsGeg)

- [2-Factor Authentication | Apps, SMS, Email, and Hardware Keys by Ken Harris](https://www.youtube.com/watch?v=26NlT1eT-U4)

- [Which 2FA method is the best? By 2FAS App](https://www.youtube.com/watch?v=iM3jc6AOCPo)

- [Two Factor Authentication (2FA). The SCAM of the Century. Defensive Strategy by Rob Braxman Tech](https://www.youtube.com/watch?v=tY7LPZbIguw)

- [Rob Braxman is WRONG about 2FA. Here’s why. by All Things Secured](https://www.youtube.com/watch?v=2kIVVEzEBHs)

- [Passwordless Authentication: Weighing the Options by IBM Technology](https://www.youtube.com/watch?v=f6LD9sDKQq8)

- [Why You Should Turn On Two Factor Authentication by Tom Scott](https://www.youtube.com/watch?v=hGRii5f_uSc)

- [What is MFA Fatigue Attack by Keytos Security](https://www.youtube.com/watch?v=tnTtx2qJkOc)