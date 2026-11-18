# Wonderland

**Platform:** TryHackMe  
**Room Name:** Wonderland  
**Difficulty:** Medium  
**Category:** Linux, Enumeration, Steganography, SSH, Privilege Escalation

---

## Introduction

In this writeup, I will explain how I completed the **Wonderland** room on TryHackMe.

During this challenge, I explored several penetration testing techniques, including network scanning, directory enumeration, steganography, source code analysis, SSH access, and Linux privilege escalation.

The main objective was to enumerate the target machine, discover hidden information, gain access to different user accounts, and finally obtain both flags.

> **Disclaimer:** This writeup is intended for educational purposes and documents my experience solving an authorized TryHackMe CTF challenge.

---

## Walkthrough

### Step 1: Network Scanning with Nmap

First, I performed a network scan against the target machine using Nmap.

The purpose of this scan was to identify open ports and discover the services running on the target system.

After analyzing the scan results, I identified the available services that could be investigated further.

![[{537F6219-45F5-418B-B288-F31F4F0B5652}.png]]
### Step 2: Directory Enumeration with Gobuster

After completing the initial network scan, I moved on to web enumeration.

I used Gobuster to discover hidden directories and files on the target web server.

During this process, I discovered interesting directories that provided additional information about the web application.

![[{E789C0A2-68B6-4AA5-9523-8D3C67815763}.png]]
### Step 3: Downloading the Rabbit Image

While exploring the website, I discovered an image of a rabbit.

I downloaded the rabbit image for further investigation because it appeared to contain potentially hidden information.


### Step 4: Steganography Analysis with Steghide

Next, I used Steghide to investigate the downloaded rabbit image.

Steghide is a steganography tool that can hide information inside image and audio files.

During the analysis, I successfully extracted a hidden file from the image.

### Step 5: Finding and Reading hint.txt

After extracting the hidden content, I discovered a file named `hint.txt`.

I read the contents of this file and found an interesting hint:

**Follow the rabbit.**

This hint gave me a direction for the next stage of enumeration.

![[{501B48F5-3101-4F1E-BC44-18F22208AB5E}.png]]
### Step 6: Exploring the Hidden Directory and Source Code

Following the hint, I explored the discovered directory.

I inspected the website's source code and found credentials that could potentially be used to access the target machine.

This information became useful in the next stage of the challenge.
![[{BE4D4631-FD7B-4FF5-A0E5-9A987AECD48D}.png]]
### Step 7: SSH Login as Alice

After discovering the credentials, I attempted to connect to the target machine using SSH.

I successfully logged in using the username **alice**.

This gave me my first initial shell access to the target machine.

![[{B6AEE99F-E19A-48E3-BE78-D70ADC54994B}.png]]

![[{1F09E11F-DA9A-4F2E-8B03-9E6DBD4BC384}.png]]
### Step 8: Finding the First Flag

After gaining access as Alice, I started exploring the filesystem.

During my enumeration, I discovered the first flag.

**Flag 1:**

`thm{"Curiouser and curiouser!"}`

![[{4F5A0DF3-A4A2-4614-AD18-7A1E8F9B4B9C}.png]]
### Step 9: Discovering the Hatter User Credentials

After finding the first flag, I continued exploring the system.

During further enumeration, I discovered another user's credentials.

The username was **hatter**, and I obtained the password required for the next login.

![[{A3144B6E-6006-469F-97CA-5EF7443BB19C}.png]]
### Step 10: SSH Login as Hatter

With the newly discovered credentials, I established another SSH connection to the target machine.

This time, I successfully logged in as **hatter**.

I now had access to a different user account and could continue investigating the system.

![[{A3144B6E-6006-469F-97CA-5EF7443BB19C} 1.png]]
### Step 11: Privilege Escalation

After logging in as Hatter, I started investigating possible privilege escalation opportunities.

I explored the system configuration, user permissions, and available resources to identify a way to gain higher privileges.

Eventually, I discovered a privilege escalation path and successfully elevated my privileges.

![[{DC625B5D-F3E4-4BE5-89D7-8AE7687BFFC4}.png]]

![[{EDF648B7-0966-4B9F-9028-C21DF127FE9D}.png]]
### Step 12: Finding the Second Flag

After successfully completing the privilege escalation, I accessed the location containing the final flag.

I found the second flag and completed the Wonderland room.

**Flag 2:**

`thm{Twinkle, twinkle, little bat! How I wonder what you’re at!}`


![[{501B48F5-3101-4F1E-BC44-18F22208AB5E} 1.png]]

---

## What I Learned

By completing this challenge, I gained practical experience with several penetration testing concepts:

- **Nmap:** Network scanning and service enumeration.
- **Gobuster:** Discovering hidden web directories.
- **Steghide:** Extracting hidden information from image files.
- **Source Code Analysis:** Identifying sensitive information in website source code.
- **SSH:** Establishing remote connections using discovered credentials.
- **Linux Enumeration:** Exploring files, directories, users, and permissions.
- **Privilege Escalation:** Identifying and exploiting a privilege escalation path in a Linux environment.

---

## Conclusion

The Wonderland room was a great learning experience. It helped me understand how different penetration testing techniques can be combined to solve a CTF challenge.

Starting with network enumeration, I moved through web directory discovery, steganography, credential discovery, SSH access, and Linux privilege escalation.

Finally, I successfully obtained both flags and completed the challenge.

**Thank you for reading my writeup!**

Happy Hacking! 🚀

**Author:** jash kania
**Platform:** TryHackMe  
**Room:** Wonderland