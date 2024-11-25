#Task1
**Perform extensive scan of the target network and identify the FQDN of the Domain Controller

nmap -p389 –sV -iL <target_list>  OR   nmap -p389 –sV <target_IP> (Find the FQDN in a subnet/network)  

nmap -sC -sV -p- -v -A -T4 -oX Oct1-24.xml <ipblock> <ipblock> <ipblock>
xsltproc Oct1-24.xml -o Oct1-24.html
