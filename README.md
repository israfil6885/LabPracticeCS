#Task1&2
**Perform an extensive scan of the target network and identify the FQDN of the Domain Controller && identify the Product Version of the Domain Controller**

nmap -sC -sV -p- -v -A -T4 -oX Oct1-24.html <IP_address>
--> look for FQDN and look for OS version 

#Task4
**Perform a vulnerability scan for the host with IP address 10.19.41.36 (je IP diye dibe oita dibo) What is the CVE number of the vulnerability with the least severity score?**

https:/10.19.41.31:8834/ --> user: wizard password: admin --> new scan --> basic network scan --> je IP scan korte bolbe oita save korbo with a specific name --> MyScan theke je naam e save koreche open kore --> launch --> report
