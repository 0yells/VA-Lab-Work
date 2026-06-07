Challenge 2 

Target 192.168.56.101

    nmap -F 192.168.56.101
    
![image alt](https://github.com/0yells/VA-Lab-Work/blob/640ec872f9fd772eb1856a157bd8579a1f2a87ba/gambar/lab8%201.png)

Found 18 open TCP ports which is (21, 22, 23, 25, 53, 80, 111, 139, 445, 513, 514, 2049, 2121, 3306, 5432, 5900, 6000, 8009).

Services include FTP, SSH, Telnet, SMTP, DNS, HTTP, NFS, MySQL, PostgreSQL, VNC, X11

MAC address shows it’s a VMware VM

Challenge 5

    ping 192.168.56.101

  ![image alt](https://github.com/0yells/VA-Lab-Work/blob/fbc7b96ceb37346dd3ee2e151353b9b9afd25838/gambar/lab8%202.png)

  Challenge 9

        nc 192.168.56.101

![image alt](https://github.com/0yells/VA-Lab-Work/blob/79147a3d7c7b11814aa2f21086d6533b0e23af23/gambar/lab8%203.png)

Challenge 17

    nmap -o 192.168.56.101

![image alt](https://github.com/0yells/VA-Lab-Work/blob/a2cbe3d1d0ef9464f15da23e7382605f1a96d792/gambar/lab8%205.png)

Challenge 19

    rpcinfo -p 192.168.56.101

![image alt](https://github.com/0yells/VA-Lab-Work/blob/54ed75e9a5b109de9d453f200c70d5a305b13344/gambar/lab8%206.png)
