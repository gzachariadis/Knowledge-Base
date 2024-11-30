#### Password Managers - Universal Option

Say, you don’t want to go the dedicated Authenticator App route, but want to use TOTP, what are your options? Well, password managers like Bitwarden Premium or Keepass offer to combine your password database and your TOTP database, offering a two-for-one solution. Pretty great right?!

Hmmm…Personally, I would avoid; Somehow having those stored in the same place doesn't sit right with me.

For one, you increase your vulnerability, having one app for both, allows for an attacker to have one vector point to attack and if successfully compromised will allow an attacker to have complete access to both aspects of your security.

Secondly, what happens if you lose access to this one place? You lost access to both your passwords/passphrases and your tokens. Single point of failure is not a good strategy!

Thirdly, it misses the point of two-factor authentication entirely, plus, what if you want to secure your password manager with a 2FA code, how do you do that, when it’s stored in the password manager, in the first place? The whole concept is alien to me and does not make sense.

My personal take? Just don’t do it.

General Usage Tips

- Two-Factor Authentication has to be performed by two separate devices. It’s inconvenient at times, but that’s security for you.

- Use a Password on your TOTP app, not biometrics. Biometrics are generally less secure than a passphrase.

- Don’t use the same password you use on your password manager, or to unlock your phone or whatever for your TOTP vault. Choose a unique, hard-to-guess long passphrase preferably.

- Do not store your backups on the cloud.

- Store at least one backup of your seeds and emergency codes off-site or somewhere you can have access in case of emergency, so in case you're travelling and get your devices stolen, you can still get in. Encrypted hard-drives or Printed QR codes aka “seeds” on a home safe is a good option.

- Active development and a reputable source are vital. Be cautious which application you choose, there’s bad actors, there’s unmaintained projects, be cautious when selecting your two-factor authentication app. You are as secure as where your seeds are stored and who can access them.

- Be cautious with cloud syncing, if you use multiple devices with sync turned on and delete something from one device, it will replicate this decision across multiple devices. That’s what sync fundamentally is.

Conclusion

While Authentication Apps are better than SMS because they are encrypted and don’t rely on your phone number, they can still be vulnerable if someone gets access to your phone or app through malware or other hacking techniques, or just general mismanagement.

To be fair to Authenticator apps, there’s no option out there that alleviates the burdens completely from your shoulder. At the end of the day, managing your TOTP Keys is mandatory, requires manual work and it’s your responsibility, and in no fault of the protocol itself; So if you want to go this route, choose an application based on your use-case and backup your seeds, preferable in more than one place.
