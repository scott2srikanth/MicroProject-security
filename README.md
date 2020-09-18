# **Micro Project - Security**
## Scope 
#### Any enterprise application generates log from multiple sources - server, client, database, network devices, external application access, gateways, OS, storage etc. Application events and attributes have to be logged to identify sequencing failures, excessive usage, meta-data changes, frauds and several other monitoring events. This project will create a pipeline into an SIEM tool that can then identify these events. The scope of this project will define two or three events that have to be identified using the SIEM. The solution can be a rule based event detection or a ML based solution to trigger or alert an undesired event. To limit the scope the project will need an application that's already generating logs, identify an SIEM tool to build a pipeline and clear definition of events, event attributes, event collection mechanism and event detection logic.
---
## Objective 
1. Learn about logs, how are they generated, and where can we find them in servers(tomcat), Linux, Windows systems?
1. Learn about events, event attributes, event collection mechanism and event detection
1. What is SIEM(System Information and Event Managment)? What are the tools available and use of SIEM pipleline
1. Installation and configuration of Splunk Enterprise tool in Linx/Windows.
1. Create a pipeline for Splunk to identify logs and events with rule based event detection.
---
## Learning
### [Logs](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/Log%20File.pdf)[, Server Logs](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/Server%20Log.pdf)
### [What is Event](https://docs.splunk.com/Splexicon:Event)[ and Event types ](https://docs.splunk.com/Documentation/Splunk/8.0.6/Knowledge/Abouteventtypes)
### [What is SIEM](https://searchsecurity.techtarget.com/definition/security-information-and-event-management-SIEM#:~:text=Security%20information%20and%20event%20management%20(SIEM)%20is%20an%20approach%20to,sim%22%20with%20a%20silent%20e.)

### [Complete Guide for SIEM](https://dnif.it/siem-security-information-event-management-guide.html#how-does-siem-work)


![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a001.png)

> Security information and event management (SIEM) is an approach to security management that combines SIM (security information management) and SEM (security event management) functions into one security management system. The acronym SIEM is pronounced "sim" with a silent e.
The underlying principles of every SIEM system is to aggregate relevant data from multiple sources, identify deviations from the norm and take appropriate action. For example, when a potential issue is detected, a SIEM system might log additional information, generate an alert and instruct other security controls to stop an activity's progress.



![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a005.png)

![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a010.png)

![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a003.png)

![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a004.png)

![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a007.png)

![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a009.png)

![SIEM](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a008.png)


### [What is Splunk](https://www.tutorialspoint.com/splunk/splunk_overview.htm)




> [Installation of Splunk Enterprise System](https://player.vimeo.com/video/139248641)

>[Creating pipeline using Universal forwader](https://player.vimeo.com/video/139401183)

![SPLUNK](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/Screenshot (84).png)

```bash
    index=main sourcetype="tomcat8serverlogs" | 
    timechart count by AccessedIP
```

![SPLUNK](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a012.png)

![SPLUNK](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a013.png)

![SPLUNK](https://raw.githubusercontent.com/scott2srikanth/MicroProject-security/master/siem/a014.png)
