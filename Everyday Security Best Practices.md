* Use a VPN …
    * … but not a free one. The idea of “if you’re not paying, you’re the product” is definitely true for commercial consumer*grade VPNs. Most collect logs about you, your browsing history, your account access details, etc. Not an ideal situation if you value your privacy.
        * If your favorite YouTuber shills it alongside HelloFresh and Raid Shadow Legends, run.
        * iCloud Private Relay is pretty good, I have no issues with it in general but prefer a dedicated 3rd party solution.
    * … paid aren’t always better but at least there’s a chance you find an ethical one.
        * I use ProtonVPN as it’s open source and paid (ie, it’s verifiably as close to zero*knowledge as a VPN provider can be while still being a functional service).
* Don’t plug in random USBs that you didn’t unwrap from the packing yourself (thanks Claire!).
    * Very common attack vector, placing crafted USBs in public places where your average user will find it, get curious, and plug it in ⇒ auto*installs my malware.
    * If you absolutely need to plug it in and access it, use the TAILS Live CD or an air gapped laptop with Qubes installed.
* Don’t ever connect to public WiFi without your VPN.
* Hover over all links to ensure the link looks legitimate.
    * On Safari, Safari main menu > View > Show Status Bar. Full URLs will now appear on bottom left when you hover over a link.
    * Other browsers have similar functionality either built in or installable via extension
    * Attack vector: An attacker can insert the following code in a webpage via XSS:
        * <a href=“[https://evil.lol](https://evil.lol/)”>Legit Site</a>
        * A normal user will see the “Legit Site” link but actually be directed to [evil.lol](http://evil.lol) if they click it.
    * Don’t click on any links you don’t recognize, esp via text, Discord, or email.
        * If you think you know the person but it seems suspicious anyway, reach out directly via a different comms channel to verify it’s actually them (impersonation is trivial).
        * If you don’t, don’t click it and call Mark.
* Never open PDFs or other attachments from unrecognized senders.
    * If you do (and esp if it’s corrupted/doesn’t open successfully/gives anything that resembles an error), run MalwareBytes and let Mark know immediately as you’ve likely been a victim of an attack.
    * Same idea as the crafted USB key.
* Use strong passwords and a password vault.
    * Best practice: 8+ characters, one upper case, one lower case, one number, one symbol
    * I use 20+ char random strings with 2 of each.
    * This site also helps: https://www.grc.com/passwords.htm
    * Most PW managers will autogenerate a good password for you - you only need to remember one password to access the vault then copy anything complex from there.
    * My preferred choice is Bitwarden, but KeePassX is also fine.
    * Never reuse passwords (old PW lists get bought and sold all the time so even if it was six passwords ago, someone somewhere is still checking if you used it).
    * Change passwords every 90 days or so.
* Use MFA - multi factor authentication - as much as you can.
    * SMS MFA is broken (SIM swaps are always a risk - I use Google Fi with Advanced Protection to mitigate the risk). It’s better than no MFA but don’t use it if there is any other option.
    * Email MFA is decent, especially if you have a strong password + MFA on your email account.
    * Best MFA option - hardware key (like Yubikey) that you physically need to have possession of before you can access an account.
        * Make sure you re*initialize the IV and other presets using the Yubico Manager utility, it’s basically a click of a button. Otherwise someone else can theoretically generate the same auth code as you.
    * Second best MFA option - authenticator app (Authy, Duo Mobile, Google Authenticator, Microsoft Authenticator). Yubikeys also offer this functionality via Yubico Authenticator, which is stored on the Yubikey itself rather than in an app.
* Hardware security:
    * Use privacy protectors and webcam covers on all your devices.
    * Lock and close all devices when you get distracted or are > 1 second from walking to reach it. Remember how they caught DPR * the FBI staged a fistfight and an agent stole his powered-on, logged-in laptop when he moved out of the way.
    * Always power off your devices when not in use. Besides the obvious difficulty of hacking a device that has no power, the Law needs to jump through more hoops to access it, plus it mitigate cold boot and evil maid attacks slightly.
* Don’t speak to the Law without a lawyer.
    * Decline to answer any questions besides basic ID things necessary to book you until you have an attorney present.
    * Don’t let them into your private space (house, car, office) without a warrant.
    * Drug dogs cost $40k+ to train and explosives dogs are more. The ones you see in the airport are 99% explosives dogs. They are expensive and valuable and aren’t meant for your average person but terrorists and cartel mules. They are bluffing if they say they’ll get a K*9 unit and “do this the hard way”, esp if it’s a car search.
    * Record all interactions  with police, esp when getting detained or pulled over. On Apple, here’s a fast and discreet way to do so: https://www.businessinsider.com/guides/tech/pulled*over*by*police*siri*shorcut*iphone?op=1 There are also dedicated apps with the same purpose.
* “Ultra secure” devices are scams.
    * It’s all marketing, a way to raise prices who are afraid of a hack but don’t actually understand your threat model yet. I used to have a Purism and it was a POS. The only real benefit is hardware kill switches but honestly buying a generic Mac in cash has the same base protections.
    * Anonymity in the crowd is the best bet. What’s easier to find - one Mac user out of 100 or the oddball out of 99 Macs and one Purism?
    * Bonus points - airgap it (never connect it to the internet at all). Transfer any required*to*install programs via a brand new USB key you took out of the packaging yourself. Won’t need updates if you never connect it to the Internet. You could even rip out the networking internals if you’re ultra paranoid.
* Other useful tricks:
    * Enable PIN Verification on ride sharing apps
    * Activate Google Advanced Protection or Apple’s Lockdown Mode.
    * Always use Incognito when browsing the internet.
    * Use an adblocker (Adguard on Safari, uBlock Origin everywhere else).
    * Use throwaway emails (anonymous free email like Proton/Google/Yahoo, Hide My Email feature on Mac, Guerrilla Mail, TemporaryMail.com) for any non*sensitive account creation and correspondence.
        * Bonus points: if you use one email per account, it’s trivial to tell who sold your data.
    * Use a webcam cover and a screen privacy protector
    * Extreme anonymity - Whonix Live CD or Tor on the TAILS live CD
    * The only antivirus worth a damn is MalwareBytes. No paid commercial ones are worth it, it’s a placebo effect.
    * Use a burner phone (Tracfone + a few 90 min prepaid cards at Walmart with cash in a location you don’t normally visit) for any situation you don’t want your number exposed. A Twilio bot helps too but isn’t as anonymous or functional.
    * Generalized OS security ranking: TAILS = Qubes > OpenBSD > MacOS/iOS > Linux = BSD > Android = Windows
