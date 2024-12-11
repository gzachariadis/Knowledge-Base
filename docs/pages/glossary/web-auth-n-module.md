# WebAuthN Authentication Module

WebAuthN (Web Authentication), a **web standard** that allows websites to authenticate users securely without relying on **Passwords**; it is what **Passkeys** rely on to verify your account ownership over **cryptographic keys**. This security module, comes pre-installed on your device as part of the Operating System. 

When you try to log in to a website, the website communicates with your device through JavaScript via the client, prompting a login action. When successful, the website and your device exchange a challenge that the device is meant to solve. Upon completion, the website verified the challenge solution and a successful login occurs.

For this process to work, both the operating system's authenticator and the device performing the login need to be in *close proximity*. This is why the authentication relies on various methods to prove proximity, such as Bluetooth, [NFC](../../../../glossary/near-field-communication.md) or USB[^1].

[^1]: Hardware connections like USB (Universal Serial Bus) are considered peripherals, therefore, proximity is not necessary and it's proved through physical connection.
