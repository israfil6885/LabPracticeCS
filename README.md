#Task1&2
**Perform an extensive scan of the target network and identify the FQDN of the Domain Controller && identify the Product Version of the Domain Controller**

nmap -sC -sV -p- -v -A -T4 -oX Oct1-24.html <IP_address>
--> look for FQDN and look for OS version 

#Task3
**Identify a machine with RDP service enabled in the 10.19.41.0/24 subnet which is Windows 10 machine. Crack the RDP credentials for user Jones. Find the file name secrect.txt You will get a hash from this file secrect.txt. Decrypt the file of hashes. Worldlists are given at parrot desktop**

nmap -p 3389 --open 10.19.41.0/24
nmap -A 10.19.41.25 10.19.41.28
(je IP er service kom sheta niye kaaj korbo- for this use the 10.19.41.25)

Now we have to find the Wordlist location (home --> parrot --> Desktop)
cd ..
cd ..
cd home
cd parrot
cd Desktop
hydra -l jones -P Wordlist.txt rdp://10.19.41.25
(command run korar por, user pass pawa jabe) 

Go to Remote Desktop Connection on your windows -->
login in this ip with the credentials --> 10.19.41.25 --> ekta text file ache, open that --> bhitore hash file thakbe, copy that --> Go to hashes.com --> paste the has file and submit to decrypt --> Then you have your answer


#Task4
**Perform a vulnerability scan for the host with IP address 10.19.41.36 (je IP diye dibe oita dibo) What is the CVE number of the vulnerability with the least severity score?**

https:/10.19.41.31:8834/ --> user: wizard password: admin --> new scan --> basic network scan --> je IP scan korte bolbe oita save korbo with a specific name --> MyScan theke je naam e save koreche open kore --> launch --> report

#Task5
** **
