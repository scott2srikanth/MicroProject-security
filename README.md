# **Micro Project - Security**

| ----------------- | ------------------------------------------------------------ |
| Summary           | In this codelab, you’ll build an installable, Progressive Web App, which loads quickly, even on flaky networks, and when launched looks like any other installed app. |
| URL               |                                             |
| Category          | Web                                                          |
| Environment       | web, security |
| Status            | Published                                                    |
| Feedback Link     |     |
| Author            | Srikanth Reddy                                               |
| Location          | KMIT                                                         |
| Analytics Account | XXXXXXXXX                                                    |

[TOC]


# Introduction to SIME

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/SIEM%20white.png?raw=true)

**Last Updated: 2020-10-05**

## What is Security information and event management (SIEM)?

Security information and event management (SIEM) is an approach to security management that combines SIM (security information management) and SEM (security event management) functions into one security management system.

The underlying principles of every SIEM system is to aggregate relevant data from multiple sources, identify deviations from the norm and take appropriate action. For example, when a potential issue is detected, a SIEM system might log additional information, generate an alert and instruct other security controls to stop an activity's progress.

## How does SIEM work?

SIEM tools work by gathering event and log data created by host systems, applications and security devices, such as antivirus filters and firewalls, throughout a company's infrastructure and bringing that data together on a centralized platform.

The SIEM tools identify and sort the data into such categories as successful and failed logins, malware activity and other likely malicious activity.

The SIEM software then generates security alerts when it identifies potential security issues. Using a set of predefined rules, organizations can set these alerts as low or high priority.

## Why is SIEM important?

SIEM is important because it makes it easier for enterprises to manage security by filtering massive amounts of security data and prioritizing the security alerts the software generates.

- Gather all your security information in 1 place to eliminate blind spots.
- Detect suspicious behaviour.
- Detects problems before they become breaches.
- Monitor and enforce policies.
- Comply to Regulatory bodies - PCI, HIPPA and FFIEC ...etc 

SIEM software enables organizations to detect incidents that may otherwise go undetected. The software analyses the log entries to identify signs of malicious activity. In addition, since the system gathers events from different sources across the network, it can recreate the timeline of an attack, enabling a company to determine the nature of the attack and its impact on the business.

A SIEM system can also help an organization meet compliance requirements by automatically generating reports that include all the logged security events among these sources. Without SIEM software, the company would have to gather log data and compile the reports manually.

For More Refer : [Complete Guide for SIEM](https://dnif.it/siem-security-information-event-management-guide.html#how-does-siem-work)

## Why explore Logs?

![](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a010.png)



Log files are the primary data source for network observability. A log file is a computer-generated data file that contains information about usage patterns, activities, and operations within an operating system, application, server or another device. IT organizations can implement security event monitoring (SEM), security information management (SIM), security information and event management (SIEM), or another analytics tool to aggregate and analyse log files from throughout a computing environment.

### Log File Categories 

#### Windows Event Logs 

The windows operating system can generate an event log in response to activity on any of its hardware or software components.

- Application Logs - an application log is created when an event takes place inside an application. These logs help code developers understand and measure how applications are behaving during development and prior to release.
- Directory Service Logs - a computer that is configured to respond to security authentication requests within a Windows Server domain (known as a domain controller) may generate directory service logs. These logs record user privilege changes, authentication operations, and requests and other operations that take place in Windows Active Directory. 
- DNS Server Logs - a Domain Name System (DNS) server contains the databases that match hostnames of websites on the internet with their appropriate IP addresses. Each time you navigate to a new web page, DNS servers are involved in processing the request and helping your browser get to the right page. DNS server logs are a special type of log file for recording activity on a DNS server. 
- File Replication Service Log - another type of log file that is only available for domain controllers, they record information about file replications that take place on the computer. 
- Security Log - security logs are created in response to security events that take place on the computer. These can include a variety of events such as failed log-ins, password changes, failed authentication requests, file deletion and more. Network administrators can configure which types of events are application events and which should be entered into the security log. 
- System Log - system logs record events that occur within the operating system itself, such as driver errors during start-up, sign-in and sign-out events and other activity

#### Linux Event Logs 

- The Linux operating system is uniquely configured to generate and store log files. Linux creates a continuous timeline of events that take place on the system, including every event related to the server, kernel, and running applications
  - Application logs 
  - Event logs 
  - Service logs 
  - System logs

## What is Event and Event types

An **event** is something that happens, especially when it is unusual or important. You can use **events** to describe all the things that are happening in a particular situation. An **event** is a planned and organized. Event is given a **timestamp**, **host**, **source**, and **source type**. Often, a single event corresponds to a single line in your inputs, but some inputs (for example, XML logs) have **multiline events**, and some inputs have multiple events on a single line. When you run a successful search, you get back events.

**Event types** are a categorization system to help you make sense of your data. Event types let you sift through huge amounts of data, find similar patterns, and create alerts and reports.

For more refer : [What is Event](https://docs.splunk.com/Splexicon:Event)[ and Event types](https://docs.splunk.com/Documentation/Splunk/8.0.6/Knowledge/Abouteventtypes)



# Introduction to Splunk Enterprise Security - SIEM Tool

Splunk Enterprise Security is an analytics-driven SIEM made of five distinct frameworks that can be leveraged independently to meet a wide range of security use cases including compliance, application security, incident management, advanced threat detection, real-time monitoring

Splunk can read this unstructured, semi-structured or rarely structured data. After reading the data, it allows to search, tag, create reports and dashboards on these data. With the advent of big data, Splunk is now able to ingest big data from various sources, which may or may not be machine data and run analytics on big data.

So, from a simple tool for log analysis, Splunk has come a long way to become a general analytical tool for unstructured machine data and various forms of data.

![](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a009.png)



![](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a008.png)

## Splunk Universal Forwarder

Universal Forwarders provide reliable, secure data collection from remote sources and forward that data into Splunk software for indexing and consolidation. They can scale to tens of thousands of remote systems, collecting terabytes of data.

Secure data collection from remote sources![secure data collection from remote sources](https://github.com/scott2srikanth/MicroProject-security/blob/master/Screenshot%2010-07-2020%2023.21.06.png?raw=true)



Forward that data into Splunk software for indexing and consolidation![](https://github.com/scott2srikanth/MicroProject-security/blob/master/Screenshot%2010-07-2020%2023.21.16.png?raw=true)



To learn more refer : [Creating pipeline using Universal forwader](https://player.vimeo.com/video/139401183)



# What you’ll build

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/ProblemStatment.png?raw=true)

## Problem Statement

Any enterprise application generates log from multiple sources - server, client, database, network devices, external application access, gateways, OS, storage etc. Application events and attributes have to be logged to identify sequencing failures, excessive usage, meta-data changes, frauds and several other monitoring events. This project will create a pipeline into an SIEM tool that can then identify these events. The scope of this project will define two or three events that have to be identified using the SIEM. The solution can be a rule based event detection or a ML based solution to trigger or alert an undesired event. To limit the scope the project will need an application that's already generating logs, identify an SIEM tool to build a pipeline and clear definition of events, event attributes, event collection mechanism and event detection logic.

## What you’ll learn

1. Learn about logs, how are they generated, and where can we find them in servers(tomcat), Linux, Windows systems?
2. Learn about events, event attributes, event collection mechanism and event detection
3. What is SIEM(System Information and Event Managment)? What are the tools available and use of SIEM pipleline
4. Installation and configuration of Splunk Enterprise tool in Linux/Windows.
5. Create a pipeline for Splunk to identify logs and events with rule based event detection.

## What you’ll need

- A recent version of Chrome (74 or later)
- Free Splunk Enterprise Tool
- Operating system : Windows/Linux/AWS Instance 
- Virtial Machine/Virtual Box (for Linux-Ubuntu)
- Splunk Universal Forworder.



# Getting set up with Splunk Enterprise Tool

Duration: 12:00

Go to Splunk.com in chrome browser.![Screenshot 10-08-2020 00.12.48](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.12.48.png?raw=true)



Click on download splunk free version.

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.13.01.png?raw=true)

# Setup with Splunk Enterprise Tool with Windows

Duration: 35:00

Download 64-bit Windows 10 installation package![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.13.26.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.13.37.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.13.54.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.07.49.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.08.07.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.08.13.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.08.29.png?raw=true)



![](https://github.com/scott2srikanth/MicroProject-security/blob/master/siem/Screenshot%2010-08-2020%2000.08.54.png?raw=true)



# Setup with Splunk Enterprise Tool with Linux

Duration: 20:00

# Splunk Enterprise Dashboard

Duration: 10:00

Navigate to localhost:8000 to open Splunk Enterprise login page![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk/Screenshot%2010-08-2020%2000.09.21.png?raw=true)



Splunk Enterprise Dashboard![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk/Screenshot%2010-08-2020%2000.09.25.png?raw=true)



# Configure Reciever

Duration: 15:00

Add a receiver for the universal forwarder.![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk/Screenshot%2010-08-2020%2000.09.44.png?raw=true)



Add new instance to receive.![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk/Screenshot%2010-08-2020%2000.09.57.png?raw=true)



Configure port number : 9997![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk/Screenshot%2010-08-2020%2000.10.08.png?raw=true)



Enable the status for the port number.![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk/Screenshot%2010-08-2020%2000.10.11.png?raw=true)



# Setup Ubuntu with VirtualBox

VirtualBox can be downloaded here: [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)

First, open VirtualBox, then click "New" to create a virtual machine.

![](https://www.freecodecamp.org/news/content/images/2019/11/start-1.png)



Enter "Ubuntu" as the name, select "Linux" as the type, and select Ubuntu (64-bit) as the version.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--14-.png)



Check the "Create a virtual hard disk now" option so we can later define our Ubuntu OS virtual hard disk size.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--16-.png)



Now, we want to select "VHD (Virtual Hard Disk)".

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--17--1.png)



Next, we'll dynamically allocate storage on our physical hard disk.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--18-.png)



Specify our Ubuntu OS's size. The recommended size is 10 GB, but you can increase the size if you wish.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--19-.png)



After creating a virtual hard disk, you'll see Ubuntu in your dashboard.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--20-.png)



The Ubuntu disk image file can be downloaded here: [Ubuntu OS download](https://ubuntu.com/#download)

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--23-.png)



To set up the Ubuntu disk image file, go to settings and follow these steps:

1. Click "Storage"
2. In storage devices, click "Empty"
3. In attributes, click the disk image and "Choose Virtual Optical Disk File"
4. Select the Ubuntu disk image file and open it



![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--25-.png)



Click OK.

Your Ubuntu OS is ready to install in VirtualBox. Let's start!

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--26-.png)



Click Install Ubuntu.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--27-.png)



Select your keyboard layout.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--29-.png)



In the "Updates and other software" section, check "Normal installation" and continue.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--30-.png)



In "Installation type", check "Erase disk and install Ubuntu".

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--31-.png)



Click "Continue".

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--32-.png)



Choose your current location.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--33-.png)



Now, set up your profile.

You'll see Ubuntu installing.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--35-.png)

After the installation, restart it.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--36-.png)

After logging in, you'll see the Ubuntu desktop.

![](https://www.freecodecamp.org/news/content/images/2019/11/Screenshot--40-.png)



# Setup Tomcat Server in Ubuntu

### Install OpenJDK

If you do not have OpenJDK or have a version older than Java 8, install the newest release by typing the following

```bash
sudo apt install default-jdk
```

```bash
java –version
```

![](https://phoenixnap.com/kb/wp-content/uploads/2019/07/check-version-java-ubuntu-tomcat.png)



### Create Tomcat User and Group

For security reasons, do not run Tomcat under the root user. Create a new group and system user to run the Apache Tomcat service from the `**/opt/tomcat**` directory.

```output
sudo groupadd tomcat
sudo useradd -s /bin/false –g tomcat –d /opt/tomcat tomcat
```

### Download Tomcat 9

1. Download the latest binary Tomcat release navigate to the [official Apache Tomcat Download page](https://tomcat.apache.org/download-90.cgi).

2. On it, find the **Binary Distributions** > **Core** list and the **tar.gz** link in it. Copy the link of the file.

![Locate latest Tomcat release.](https://phoenixnap.com/kb/wp-content/uploads/2019/07/latest-binary-tomact-release-download.png)

3. Go back to the terminal and change to the `**/tmp**` directory with the command:

```output
cd /tmp
```

4. Now, use the `**curl**` command with the **tar.gz** link you copied in step 2 to download the package:

```output
curl -O https://downloads.apache.org/tomcat/tomcat-9/v9.0.37/bin/apache-tomcat-9.0.37.tar.gz
```

![Use the curl command to download the Tomcat package.](https://phoenixnap.com/kb/wp-content/uploads/2019/07/tar-gz-tomcat-curl-ubuntu-download.png)

### Extract tar.gz File

1. To extract the tar.gz Tomcat file, create a new `**/opt/tomcat/**` directory with the command:

```output
sudo mkdir /opt/tomcat
```

2. Then, extract the file in the new directory with the following command:

```output
sudo tar xzvf apache-tomcat-9*tar.gz –C /opt/tomcat –strip-components=1
```

![Extract tar.gz file.](https://phoenixnap.com/kb/wp-content/uploads/2019/07/extract-tar-gz-tomcat-file-ubuntu.png)

### Modify Tomcat User Permission

The new Tomcat user you created does not have executable privileges, but it needs to access the installation directory. You need to setup execute privileges over the directory.

1. Move to the directory where the Tomcat installation is located:

```output
cd /opt/tomcat
```

2. Grant group ownership over the installation directory to the `**tomcat**` group with the command:

```output
sudo chgrp –R tomcat /opt/tomcat
```

3. Also, give it read access to the `**conf**` directory and its contents by typing:

```output
sudo chmod –R g+r conf
```

4. Followed by [changing directory permissions](https://phoenixnap.com/kb/linux-file-permissions) to grant execute access with:

```output
sudo chmod g+x conf
```

5. Finally, give the tomcat user ownership of the `**webapps**`, `**work**`, `**temp**`, and `**logs**` directories using the command:

```output
sudo chown –R tomcat webapps/ work temp/ logs
```

![tomcat user permissions modified](https://phoenixnap.com/kb/wp-content/uploads/2019/06/word-image-32.png)

### Create System Unit File

Since you are going to to use Tomcat as a service, you need to create a **systemd service file**.

1. To configure the file, you first need to find the “`JAVA_HOME`” path. This is the exact location of the Java installation package.

To do so, prompt the system to give you information about the Java packages installed on the system. In the terminal, type:

```output
sudo update-java-alternatives -1
```

![Create a systemd service file.](https://phoenixnap.com/kb/wp-content/uploads/2019/07/create-systemd-service-file.png)

As the output shows, there are two available versions of Java. Accordingly, it also shows two paths displaying their location.

Choose the version you want to use and copy its location. With that, you can move on to create the service file.

\2. Create and open a new file in the **/etc/system/system** under the name **tomcat.service**:

```output
sudo nano /etc/systemd/system/tomcat.service
```

3. Once the file opens, copy and paste the content below, changing the **JAVA_HOME** value to the information you found in the previous step.

```output
[Unit]
Description=Apache Tomcat Web Application Container
After=network.target

[Service]
Type=forking

Environment=JAVA_HOME=/usr/lib/jvm/java-1.11.0-openjdk-amd64
Environment=CATALINA_PID=/opt/tomcat/latest/temp/tomcat.pid
Environment=CATALINA_HOME=/opt/tomcat
Environment=CATALINA_BASE=/opt/tomcat
Environment=’CATALINA_OPTS=-Xms512M –Xmx1024M –server –XX:+UserParallelGC’
Environment=’JAVA_OPTS=-Djava.awt.headless=true Djava.security.egd=file:/dev/./urandom’

ExecStart=/opt/tomcat/bin/startup.sh
ExecStop=/opt/tomcat/bin/shutdown.sh

User=tomcat
Group=tomcat
UMast=0007
RestartSec=10
Restart=always

[Install]
WantedBy=multi-user.target
```

![Change Java-Home value.](https://phoenixnap.com/kb/wp-content/uploads/2019/07/java-home-value-tomcat-service-ubuntu.png)

4. **Save** and **Exit** the file (**Ctrl+X**, followed by **y**[es] and **Enter**).

5. For the changes to take place, reload the system daemon with the command:

```output
sudo systemctl daemon-reload
```

6. Now, you can finally start the Tomcat service:

```output
sudo systemctl start tomcat
```

7. Verify the Apache Tomcat service is running with the command:

```output
sudo systemctl status tomcat
```

The message you want to receive is that the service is **active (running)**.

### Adjust Firewall

If you are using a firewall to protect your server (as you should), you will not be able to access the Tomcat interface. Tomcat uses Port 8080, which is outside your local network.

1. Open Port 8080 to allow traffic through it with the command:

```output
sudo ufw allow 8080/tcp
```

2. If the port is open, you should be able to see the Apache Tomcat splash page. Type the following in the browser window:

**http://localhost:8080**

Your web browser should open the web page as in the image below:

![Apache Tomcat Splash Page](https://phoenixnap.com/kb/wp-content/uploads/2019/07/apache-tomcat-splash-page-ubuntu.png)





# Setup Splunk Universal Forwarder in Ubuntu for tomcat logs.

Download Universal forwarder for splunk - https://www.splunk.com/en_us/download/universal-forwarder.html#tabs/linux

Download tgz file.

1. Open ternimal and type the command:

```bash
cd Downloads
sudo tar xvzf splunkforwarder.tgz -C /opt
```

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk%20forworder/Screenshot%2010-07-2020%2023.24.39.png?raw=true)



```bash
cd /opt/splunkforworder/bin
sudo ./splunk start --accept-license
```

Provide admin username and password(default: username : admin and password : adminadmin)

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk%20forworder/Screenshot%2010-07-2020%2023.25.09.png?raw=true)

Splunk service started.

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk%20forworder/Screenshot%2010-07-2020%2023.25.29.png?raw=true)

Start splunk service at boot up.

```
sudo ./splunk enable boot-start
```

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk%20forworder/Screenshot%2010-07-2020%2023.25.43.png?raw=true)

Set the forwarder to send data to Splunk Enterprise server.

```
sudo ./splunk add forward-server 10.16.28.53:9997
```

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk%20forworder/Screenshot%2010-07-2020%2023.26.02.png?raw=true)

![](https://github.com/scott2srikanth/MicroProject-security/blob/master/splunk%20forworder/Screenshot%2010-07-2020%2023.26.08.png?raw=true)

```
sudo ./splunk add monitor /opt/tomcat/logs
```

# Splunk Events and Log Analysis.

```
index=main sourcetype="tomcat8serverlogs" | timechart count by AccessedIP
```

![](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a012.png)



![](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a013.png)

Log Visualization

![](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a014.png)
