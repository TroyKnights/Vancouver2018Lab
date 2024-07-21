<h1>Kali Linux/ Vancouver 2018 Exploitation</h1>


<h2>Description</h2>
This project uses Kali Linux Tools along with wireshark to exploit a "Vancouver 2018" test virtual machine and gain root access to retreive a file. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Nmap</b> 
- <b>Wordlist</b>

<h2>Environments Used </h2>

- <b>Kali Linux</b>
- <b>VMware</b> 

<h2>Program walk-through:</h2>

<p align="center">
1. I started by using Netdiscover to find the Ip address of the machine I am attacking<br/>
  <br/><br/>
<img src="https://i.imgur.com/ecI5r3M.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
2. I used Nmap to find vulnerable ports to exploit <br/>
  <br/><br/>
<img src="https://i.imgur.com/UzHHSpt.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
3. Accessed the vulnerable ftp port  <br/>
  <br/>Vulnerabilities found in ftp port 21, ssh port 22 and http port 80 <br/>
  <br/><br/>
<img src="https://i.imgur.com/lMVE5Ag.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
4. Took user.txt from the ftp server <br/>
  <br/><br/>
<img src="https://i.imgur.com/o4DqbTV.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
5.Tried to use the usernames to open ssh. All usernames denied except anne. <br/>
  <br/><br/>
<img src="https://i.imgur.com/4EI9bU4.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
6. Used the rockyou wordlist located in Kali linux to find the password for anne<br/>
  <br/><br/>
<img src="https://i.imgur.com/iQUsrzq.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
7.I logged into then ssh port using the password I found. I used sudo -l to figure out permissions. Anne had permission to run anything. I used sudo /bin/sh to enter the root folder. Once I was given root access I found the flag <br/>
  <br/><br/>
  <img src="https://i.imgur.com/6slqqeK.png" height="80%" width="80%" alt="Vancouver2018"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
