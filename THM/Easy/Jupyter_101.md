# Jupyter 101

A friendly introduction into using the Jupyter Notebook environment. Learn to process and visualise data!

This is a Data Science related room...

## Task 1 - Preface

Only reading...

## Task 2 - What is Jupyter? 

Only reading...

## Task 3 - Deploying Instance & Logging In 

The description says that I need to wait 5 minutes for the machine to boot correctly...

It also says that we have to:

**Use the password: *tryhackme***

Target IP: 10.10.111.168

I do the initial ennumeration with nmap:

**nmap -sV -A 10.10.111.168**

~~~
Starting Nmap 7.80 ( https://nmap.org ) at 2020-08-02 18:49 EDT                                                                                                
Nmap scan report for 10.10.111.168                                                                                                                             
Host is up (0.20s latency).                                                                                                                                    
Not shown: 997 closed ports                                                                                                                                    
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 10:52:11:e8:f4:c0:a6:be:1c:7c:59:a9:fb:89:35:71 (RSA)
|   256 6b:00:77:d8:64:d7:cb:a7:2e:22:8b:3d:b7:81:5d:26 (ECDSA)
|_  256 04:2d:3d:c0:c0:f1:50:b9:cb:45:ec:5a:d7:72:f2:b6 (ED25519)
80/tcp   open  http    nginx 1.14.0 (Ubuntu)
| http-robots.txt: 1 disallowed entry 
|_/ 
|_http-server-header: nginx/1.14.0 (Ubuntu)
| http-title: Jupyter Notebook
|_Requested resource was /login?next=%2Ftree%3F
8888/tcp open  http    Tornado httpd 6.0.3
| http-robots.txt: 1 disallowed entry 
|_/ 
|_http-server-header: TornadoServer/6.0.3
| http-title: Jupyter Notebook
|_Requested resource was /login?next=%2Ftree%3F
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 25.47 seconds
~~~

I open the URL in port 80:

**http://10.10.111.168/**

And I get the login page, asking only for a "Password". I enter the one provided by the task description "tryhackme".

I get the "Home Page - Select or create a Notebook" page.

The link to the supporting material in the task description is dead...

## Task 4 - Let´s learn More About Jupiter

Task Description:

> Enter the "WhatIsJupyter" directory and launch "WhatIsJupyter.ipynb" and have a read through.<br>
> There's no questions, but I detail some use cases of Jupyter and why someone might use it over an IDLE such as PyCharm! 


Not much to do here, just reading...

## Task 5 - Understanding how Jupiter Notebooks Run


