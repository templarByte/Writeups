# <img src="imgs/jupyterlogo.png" alt="Jupyter room logo at TryHackMe" width="80"/> Jupyter 101

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

### 1. What do "Cell" act like?

Reading the contents of the document...

**interpreter**

### 2. What would be the In[#] value of the first Cell when it is ran for the first time? (Where # would be the numerical value)

In the document previously opened, I find the referenced values on the left side of each Cell...

**1**

### 3. What keyboard shortcut can you press to execute a cell?

Checking the Help Menu, I find the "Keyboard shortcuts" option...

**Shift + Enter**

### 4. If you was to execute the first Cell again, what would the value of In[#] now become? (Where # would be the numerical value)

I press the "Run" botton twice, since I didn´t do it previously...

**2**

## Task 6 - Interacting with the Filesystem!

The task description asks to **ssh** login with the following credentials:

> Username: thm
> Password: tryhackme

So, I do it like this...

***ssh -l thm 10.10.111.168***

~~~
The authenticity of host '10.10.111.168 (10.10.111.168)' can't be established.
ECDSA key fingerprint is SHA256:Hy75v4qT0TD6cCRRbTv/r5/NZRMnP+2Eqm/a/91xzoM.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.10.111.168' (ECDSA) to the list of known hosts.
thm@10.10.111.168's password: 
~~~

**ls**

~~~
thm@thm-jupyter101-vm:~$ ls
'Interesting Notebooks'   IntroToMatplotlib   IntroToPandas   socials.txt   UnderstandingJupyterNotebooks   WhatIsJupyter
thm@thm-jupyter101-vm:~$ 
~~~

The task description asks to create a file there...

**touch LookAtMe.txt**

~~~
thm@thm-jupyter101-vm:~$ ls
'Interesting Notebooks'   IntroToMatplotlib   IntroToPandas   LookAtMe.txt   socials.txt   UnderstandingJupyterNotebooks   WhatIsJupyter
thm@thm-jupyter101-vm:~$ 
~~~

And I verify that it shows in the web browser...

I enter the well known *"Hello World!"* text, and go to "File" > "Save" in the web browser.

I verify it in the terminal with:

**cat LookAtMe.txt**

~~~
Hello World!
~~~

## Task 7 - Handling Data with Pandas

I open the "IntroToPandas" directory in the web browser and run the "IntroToPandas.ipynb" document to read it's contents.

### 1. What are the two main types of data within Pandas?

I find this information in the very first page...

**series and dataframes**

### 2. What is the name of the Pandas function that reads a CSV file?

I notice this information under In [7]...

**read_csv**

### 3. Name the Pandas function you would use if you only wanted to display the first few rows

I find this under In [9]

**head**

### 4. Name the Pandas function you would use if you only wanted to display the last few rows

This can be found under In [10]...

**tail**

### 5. What Pandas function will give you a numerical count of the amount of columns and rows the dataset contains?

This is under In [11]:

**shape**

## Task 8 - Visualizing Data With Matplotlib

I open the "IntroToMatplotlib" directory, and run the "IntroToMatplotlib.ipynb" document to read the annotations there...

### 1. How do you display a plot? 

This is mentioned at In [3]

**plot()**

### 2. How would you label the "x" axis on a plot?

Above In [5]:

**xlabel**

### 3. How would you label the "y" axis on a plot?

Following the pattern...

**ylabel**

### 4. How would you add a "Title" to a plot?

Found at In [5]

**title**

### 5. What word would you use to change the color of the plot?

Found at In[7]:

**color**

### 6. How would you label the "z" axis on a plot?

Following the pattern...

**zlabel**


That´s it, room finished.
