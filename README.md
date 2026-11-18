# 🐇 TryHackMe - Wonderland Writeup

!Platform !OS !Category !Status

## 📌 About the Room

**Wonderland** is a Linux-based Capture The Flag (CTF) challenge available on TryHackMe.

In this challenge, I explored different penetration testing techniques, including network scanning, directory enumeration, steganography, credential discovery, SSH access, Linux enumeration, and privilege escalation.

The objective was to enumerate the target machine, discover hidden information, gain access to different user accounts, and retrieve both flags.

- **Platform:** TryHackMe
- **Room:** Wonderland
- **Operating System:** Linux
- **Difficulty:** Medium
- **Tools Used:** Nmap, Gobuster, Steghide, SSH

---

## 🛠️ Tools Used

|Tool|Purpose|
|---|---|
|Nmap|Network scanning|
|Gobuster|Directory enumeration|
|Steghide|Extracting hidden files from images|
|SSH|Remote machine access|
|Linux Commands|System enumeration and privilege escalation|

---

## 🚀 Walkthrough

### Step 1 - Network Scanning

Started by scanning the target IP address using Nmap to identify open ports and running services.

### Step 2 - Directory Enumeration

Used Gobuster to discover hidden directories and files on the target web server.

### Step 3 - Downloading the Rabbit Image

During website enumeration, discovered a rabbit image and downloaded it for further analysis.

### Step 4 - Steganography Analysis

Used Steghide to investigate the rabbit image and successfully extracted a hidden file.

### Step 5 - Reading the Hint File

Found the `hint.txt` file after extraction.

Read the file and discovered the following clue:

**Follow the rabbit.**

### Step 6 - Source Code Analysis

Followed the discovered directory and inspected the website's source code.

Found credentials in the source code that could be used for further access.

### Step 7 - SSH Login as Alice

Used the discovered credentials to establish an SSH connection to the target machine.

Successfully logged in as **Alice**.

### Step 8 - First Flag

After gaining access as Alice, explored the filesystem and successfully found the first flag.

### Step 9 - Discovering Hatter Credentials

Continued enumerating the machine and discovered another user's credentials.

The username was **Hatter**.

### Step 10 - SSH Login as Hatter

Used the discovered credentials to connect through SSH as Hatter.

Successfully obtained access to the Hatter user account.

### Step 11 - Privilege Escalation

Started investigating the system for privilege escalation opportunities.

After analyzing the available permissions and system configuration, discovered a privilege escalation path and successfully gained higher privileges.

### Step 12 - Second Flag

After completing privilege escalation, accessed the final flag location.

Successfully retrieved the second flag and completed the Wonderland challenge.

---

## 🏁 Flags

|Flag|Status|
|---|---|
|User Flag|✅ Captured|
|Root Flag|✅ Captured|

---

## 📚 What I Learned

Through this challenge, I improved my practical knowledge of:

- Network scanning using Nmap.
- Web directory enumeration using Gobuster.
- Steganography and hidden file extraction using Steghide.
- Analyzing website source code for sensitive information.
- Finding and using credentials.
- Connecting to Linux machines using SSH.
- Linux filesystem and user enumeration.
- Linux privilege escalation techniques.

---

## 🎯 Conclusion

Wonderland was an interesting and enjoyable CTF challenge that helped me understand how multiple penetration testing techniques work together.

From initial network scanning to privilege escalation, every step provided a valuable learning experience.

I successfully obtained both flags and completed the room.

**Happy Hacking! 🐇**

---

## 🔗 References

- [TryHackMe](https://tryhackme.com/)
- [Nmap Documentation](https://nmap.org/book/man.html)
- [Gobuster GitHub](https://github.com/OJ/gobuster)
- [Steghide Documentation](https://steghide.sourceforge.net/)

---

**Author:** Your GitHub Username  
**Platform:** TryHackMe  
**Challenge:** Wonderland

_This writeup is intended for educational purposes and documents an authorized CTF lab experience._
