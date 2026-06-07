Challenge 2 

Target 192.168.44.131

    nmap -F 192.168.44.131
    
![image alt](https://github.com/0yells/VA-Lab-Work/blob/640ec872f9fd772eb1856a157bd8579a1f2a87ba/gambar/lab8%201.png)

Found 18 open TCP ports which is (21, 22, 23, 25, 53, 80, 111, 139, 445, 513, 514, 2049, 2121, 3306, 5432, 5900, 6000, 8009).

Services include FTP, SSH, Telnet, SMTP, DNS, HTTP, NFS, MySQL, PostgreSQL, VNC, X11

MAC address shows it’s a VMware VM

Challenge 5

    ping 192.168.44.131

  ![image alt](https://github.com/0yells/VA-Lab-Work/blob/fbc7b96ceb37346dd3ee2e151353b9b9afd25838/gambar/lab8%202.png)

  Challenge 9

        nc 192.168.44.131

![image alt](https://github.com/adammsyabill/VA-Lab-Work/blob/141a6783128c9d5715a32eff73c5a62ad13303ab/image/Screenshot%202026-06-05%20004826.png)

Challenge 17

    nmap -o 192.168.44.131

![image alt](https://github.com/adammsyabill/VA-Lab-Work/blob/073dbc8f1ab2810148b3559dbc8b5ddc65b5e0f2/image/Screenshot%202026-06-05%20005103.png)

Challenge 19

    rpcinfo -p 192.168.44.131

![image alt](https://github.com/adammsyabill/VA-Lab-Work/blob/85c1feb7c9d71207aa0bd251f9aff83c671d6bc1/image/Screenshot%202026-06-05%20005311.png)
