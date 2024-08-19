# UFW Firewall Configuration Project

This project demonstrates the setup and configuration of a firewall using UFW (Uncomplicated Firewall) on a Linux system. The configuration includes various rules for allowing and denying traffic, as well as some basic UFW management commands.

## Table of Contents
1. [Installation](#installation)
2. [Basic Configuration](#basic-configuration)
3. [Port Rules](#port-rules)
4. [IP-based Rules](#ip-based-rules)
5. [Logging and Status](#logging-and-status)
6. [Default Policies](#default-policies)
7. [Application Rules](#application-rules)

## Installation

#### Update your system
- sudo apt update
- sudo apt upgrade -y
#### Install UFW 
- sudo apt install ufw
![App Screenshot]('./images/one.png')

#### Enable ufw 
- sudo ufw enable
![App Screenshot]('./images/two.png')
 
#### Allow ssh  Connections
 - sudo ufw allow ssh
 ![App Screenshot]('./images/three.png')
##### Alternatively you could specify the port :
 - ufw allow 22/tcp
  ![App Screenshot]('./images/four.png')
  
## Allowing specific Services:


#### Allow Http and Https Connections
 - ufw allow http
- ufw allow https
- ufw allow 80/tcp
- ufw allow 443/tcp
![App Screenshot]('./images/five.png')
![App Screenshot]('./images/six.png')

#### Allowing other specific ports 
- ufw allow 8080/tcp
- ufw allow 1000:2000/tcp
![App Screenshot]('./images/seven.png')
![App Screenshot]('./images/eight.png')

#### Allowing other specific Ip address 
- ufw allow from 192.255.127.163
![App Screenshot]('./images/nine.png')
#### Allowing other specific Subnets:
- ufw allow from 192.168.1.0/24
![App Screenshot]('./images/ten.png')

#### Deny Specific Services and ports:
- ufw deny 23/tcp
![App Screenshot]('./images/11.png')
#### Deny Specific Ip address:
- ufw deny from 203.0.113.0
![App Screenshot]('./images/12.png')
 
## View UFW Status and Rules:
- sudo ufw status verbose
![App Screenshot]('./images/13.png')
#### Using the number Rule :
- sudo ufw staus numbered 
#### Deleting a rule using numbered :
- ufw delete 6
![App Screenshot]('./images/14.png')
#### Using specific rules:
- sudo ufw status delete allow 8080/tcp


## Advanced UFW Configuration:
####Logging :
- ufw logging on
![App Screenshot]('./images/15.png')
#### Default Policies:
- ufw default deny incoming
- ufw default allow incoming
- ufw default deny outgoing
- ufw default allow outgoing
![App Screenshot]('./images/16.png')
####  Applicatication Profiles:
- sudo ufw applist 
![App Screenshot]('./images/17.png')
##### Allow specific apps:
- sudo  ufw allow 'Nginx Full'





