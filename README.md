#Task1&2
**Perform an extensive scan of the target network and identify the FQDN of the Domain Controller && identify the Product Version of the Domain Controller**
$ nmap -sC -sV -p- -v -A -T4 -oX yourname.xml  10.19.41.0/24
nmap -sC -sV -p- -v -A -T4 -oX Oct1-24.xml <IP_address>
--> look for FQDN and look for OS version 

#Task3
**Identify a machine with RDP service enabled in the 10.19.41.0/24 subnet which is Windows 10 machine. Crack the RDP credentials for user Jones. Find the file name secrect.txt You will get a hash from this file secrect.txt. Decrypt the file of hashes. Worldlists are given at parrot desktop**

nmap -p 3389 --open 10.19.41.0/24
nmap -A 10.19.41.25 10.19.41.28
(je IP er service kom sheta niye kaaj korbo- for this use the 10.19.41.25)

Now we have to find the Wordlist location (home --> parrot --> Desktop)
cd ..
cd parrot
cd Desktop
hydra -l jones -P Wordlist.txt rdp://10.19.41.25
(command run korar por, user pass pawa jabe) 

--> Go to Remote Desktop Connection on your windows 
--> login in this ip with the credentials 
--> 10.19.41.25 
--> ekta text file ache, open that 
--> bhitore hash file thakbe, copy that 
--> Go to hashes.com 
--> paste the has file and submit to decrypt 
--> Then you have your answer


#Task4
**Perform a vulnerability scan for the host with IP address 10.19.41.36 (je IP diye dibe oita dibo) What is the CVE number of the vulnerability with the least severity score?**

https:/10.19.41.31:8834/ 
--> user: wizard password: admin 
--> new scan 
--> basic network scan 
--> je IP scan korte bolbe oita save korbo with a specific name 
--> MyScan theke je naam e save koreche open kore 
--> launch 
--> report

#Task5
**A file named Secret.txt has been uploaded through DVWA (http://10.19.41.36/vulnerabilities/upload/). The file is located in the "C:\wamp64\www\DVWA\hackable\uploads\" directory. Access the file and crack the MD5 hash to reveal the original message. Enter the decrypted message as the answer. You can log into the DVWA using the credentials admin/password**

--> hit http://10.19.41.36
--> user:admin/password:password 
--> set dvwa security to "low" and click submit 
--> go to "upload"
--> upload any small file (low quality image/ text file)
--> upload korar por ekta url ashbe niche oitar just "../../hackable/uploads/" ei tuku copy kore will paste after "http://10.19.41.36"
--> browser e hit korbo 
--> open secret.txt file 
--> hash file niye hashes.com theke decrypt korbo 
--> Then you have your answer


