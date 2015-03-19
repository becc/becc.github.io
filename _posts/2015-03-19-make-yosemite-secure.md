---
layout: post
title: Make OSX Yosemite Secure
---


Secure Your Mac (Yosemite)

These steps will help keep data on your mac safe even if it’s stolen or your iTunes account is hacked. They come from [Apple](https://support.apple.com/kb/PH18891?locale=en_US) and the [NSA](http://www.nsa.gov/ia/_files/factsheets/macosx_10_6_hardeningtips.pdf) ([updated](http://www.macworld.com/article/2048160/how-the-nsa-snoop-proofs-its-macs.html)).

# Don’t Surf or Read Mail Using Admin Account

Create a non-administrator user in the Users & Groups pane of System Preferences and use this account for everyday tasks. Only log in with an administrator account when you need to perform system administration tasks.

# Use Software Update

Maintaining up to date software is extremely important.

Go to “System Preferences -> App Store” and tick every box listed under “Automatically check for updates.”

# Account Settings

For the following tasks, open the “Users and Groups” pane in System Preferences and select “Login Options.”


Without strong passwords, it's trivial to steal your data.

1. Set password – For each user
    * Click “Change Password” and select “Use Separate Password” or “Change Password” (Do not select “Use iCloud Password...”)
    * Choose a very secure password > 12 chars.
    * Use a passphrase like “Oh! My f0x bit the fish!”
      See http://xkcd.com/936/
    * Easy to type, hard to guess, very hard to brute force.

2. Don't leave the door unlocked
  * Automatic login: Off
  * Display login window as: Name and password
  * Uncheck all boxes.

3. Disable the guest user
  * Select the “Guest User”
  * Uncheck “Allow guests to log in to this computer.”
  * Uncheck “Allow guest users to connect to shared folders.”

# Security Pane Settings

Open the “Security & Privacy” pane in System Preferences.

1. Automatically lock your screen when you're away
  * Select “General” tab.
  * Check “Require password 1 minute after sleep or screen saver begins.

2. Make malware difficult to install
  * Select “General” tab.
  * Select “Mac App Store and identified developers.

3. Encrypt your disk
  * Select FileVault and click “Turn On FileVault.” 
  * Select the user accounts you want to allow to log in to the computer. 
  * Write down the displayed recovery key. 
    Keep this key in case you forget your password, because it’s the only way you carecover your data.
  * Select “Do not store the recovery key with apple.”

4. Turn on the firewall
  * Select the Firewall tab.
  * Click “Turn On Firewall.”
  * Select “Firewall Options” and
  * check “Block all incoming connections.”

5. Make yourself private
  * Select the “Privacy” tab and 
  * uncheck “Enable Location Services.” 
  * Open “Diagnostics & Usage” and 
  * uncheck “Send diagnostics & usage data to Apple.”

# Prevent a hacker from wiping your computer

1. Open the "iCloud" Pane in System Preferences
  * Uncheck “Back to My Mac” 
  * Uncheck “Find My Mac” to prevent a hacker from wiping your drive. 


Doing these items make your system more secure than most. Remember, when you're running from a bear, you don't have to be the fastest, just don't be the slowest.
