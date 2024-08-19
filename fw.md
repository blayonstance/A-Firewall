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
![App Screenshot]('./')

#### Enable ufw 
- sudo ufw enable
![App Screenshot]('./')
 
 #### Allow ssh  Connections
 - sudo ufw allow ssh
 ##### Alternatively you could specify the port :
 - ufw allow 22/tcp
  ![App Screenshot]('./')
  ## Allowing specific Services


 #### Allow Http and Https Connections
 - ufw allow http
- ufw allow https
- ufw allow 80/tcp
- ufw allow 443/tcp
![App Screenshot]('./')
#### Allowing other specific ports 

