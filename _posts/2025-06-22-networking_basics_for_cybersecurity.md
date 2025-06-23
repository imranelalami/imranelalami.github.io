---
layout: post
title: Basic Networking for CyberSecurity
date: 2025-06-22 12:00:00 +0100
categories:
  - Networking
  - Learning
tags:
  - Protocols
description: Some Protocols and Pre knowledge you need to know to get in CTFs and Cybersec
image: /assets/img/Learning/Networks.png
---

Cybersecurity is a vast field, it is like an ocean with various depths. So to get your tippy toe into this field one of the first things you'll need to study before hacking is Networking. In this blog I'll try my best to help you get some basic knowledge of networking to get started with CTFs or to start learning how to hack stuff. As I said this is nothing but an introduction so any beginner must do some digging on each subject here if he/she wants to get real invested into ethical hacking or penetration testing.

# What Is Networking and why should i learn it

Networking in IT is the process of communication between devices. You need to fully know how they talk, how each command or message or email is sent/received in order to get a good grasp of how these combination of rocks and sand can display and stream your anime waifu in 4k.. aaand maybe hack some of them?!

![wifu](/assets/img/Learning/wifu.jpeg) 

---

These devices talk to each other in what is called (you guessed it) a network. So just like us humans, we can talk to the person in front of us by whispering or talk to the person in the other room by shouting or talk to the person in the other city through a phone call, devices also talk to each other using different methods or a combination of methods depending on the type of network.

# Types of networks


![types](/assets/img/Learning/types_of_networks.png)


There are different types of networks. I'll explain them briefly in order to not overwhelm you with too much information you don't need right now.

## PAN

Personal Area Network . connects devices within a person's immediate area, typically 1-10 meters. Uses Bluetooth, infrared, or Zigbee protocols. Common devices include smartphones, headphones, smartwatches, and fitness trackers. (imagine you sending a video to your friend over Bluetooth , yeah that's also a network)

## LAN

Local Area Network. covers a small geographic area like your home, office, or a uni building. Uses Ethernet cables or WiFi. Typically operates on private IP ranges (192.168.x.x, 10.x.x.x). Managed by switches and connected to internet via devices called routers ( more on all of that later).

## WAN

Wide Area Network. it's like a big road system that connects computers in different cities or countries. It's used to link smaller networks together, like connecting homes, offices, or schools that are far apart. The biggest example of a WAN is the internet we have today ( it is the largerst network of them all)

## WLAN

You already know this, Wireless Local Area Network,  just like a LAN that uses wireless communication instead of cables. basically your WIFI

## MAN

Metropolitan Area Network. covers a city or large campus area. Larger than LAN but smaller than WAN. Often uses fiber optic cables and is owned by ISPs or large organizations.

## GAN

Global Area Network. spans multiple WANs across continents. Uses satellite communications and undersea cables. Provides global connectivity for multinational organizations.. you'll probably wont need to worry about this.


---

These networks have all sorts of devices inside them: laptops, phones, tablets, heck even your light bulb that automatically sends traffic to China. So in order for these devices to talk to each other and for these networks to also talk to each other we need some Network Devices.

# Networking Devices

![devices](/assets/img/Learning/devices.jpeg)

As I said, in order for your phone for example to send a meme to your friend across the country you need networks and these are linked with and rely on some devices that are specifically designed for that purpose. Some of them make your network safer, some of them make your LAN network talk to other LAN networks and some of them facilitate the file transfer between your laptop and your desktop in the same building.

## Switches

These are devices that connect devices within a LAN. you plug all your wired stuff in one these and they remember who is connected where, so they can send messages to the right device. Each connection on the switch works separately, so devices don’t "bump into" each other when talking. ps: they work very fast.

## Routers

these are like that policeman standing on the road to facilitate the movment of cars , They route packets between different networks using IP addresses.. They read the address on each message and decide the best way to send it. They also let many devices in your home share one internet connection using something called NAT(more on that later).

## Modems

Modulate digital signals to analog for transmission over telephone lines, cable, or fiber. basically They change the digital signals from your computer into signals that can travel through cables, or fiber lines and then change them back again so your computer can understand.

## Access Points (AP)

Wireless devices let phones, laptops, and other wireless devices connect to the internet without needing a cable. they extend wired networks to wireless clients
 They can also create different "Wi-Fi names" for guests or different parts of a building.
 
## Firewalls (god forbid)

Firewalls are like security guards for a network. They watch the internet traffic coming in and the traffic going out, and decide what to let through and what to block based on a list of rules.
Some firewalls just check the basics, and others are smarter and look deeper into the traffic to keep you safer. They help protect your computer or network from unwanted or dangerous visitors but can be pain in the ass sometimes.

---

And there are so many devices that build up a network's Network Infrastructure (seriously networking guys love their gadgets). But all those fancy pieces of metal would be useless without a proper way of.. well actually talking to each other and facilitating the communication between other pieces of metal. Here comes the most important part for you hackerman: **protocols**.

# Protocols

![protocols](/assets/img/Learning/protocols.png)

In our previous analogy, I said that you can whisper to your friend next to you or shout to the friend in the other room. That thing you do with your mouth (talking) usually needs a language for it in order for both parties to understand each other. Computers need that too. These are Protocols - they are the language of networks. They let devices understand each other and share data reliably.


## IP (Internet Protocol)


<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/5WfiTHiU4x8?si=6u8aNdft3MbaemFB" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


The Internet Protocol is what allows devices to find and communicate with each other over a network. It gives each device a unique address, called an IP address, which is like a home address for computers. When data needs to be sent across networks—whether it's a web page, a video, or a message—IP helps break that data into smaller chunks called packets and routes them from the sender to the receiver. If a packet is too big, IP can split it up and reassemble it at the destination. IP doesn’t guarantee delivery, timing, or order—it just does its best to push the packets toward the right place. There are two versions: IPv4, which is older and uses shorter addresses like “192.168.1.1,” and IPv6, which uses much longer addresses to support the growing number of devices on the internet.



## ICMP (Internet Control Message Protocol)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/5EP1NZAu_PQ?si=kxt-VegR2MF-g3w0" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


ICMP is a helper protocol used mainly for sending error messages and performing diagnostics on a network. It doesn’t carry user data like websites or files—instead, it helps devices report problems. For example, when you use the "ping" command to test if a server is reachable, your computer sends an ICMP Echo Request, and if the server is alive and reachable, it sends back an Echo Reply. If a router along the path is down or the destination is unreachable, ICMP can send back a message to let the sender know. It’s part of the Internet layer, just like IP, and plays a key role in network troubleshooting and communication health checks.



## ARP (Address Resolution Protocol)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/aamG4-tH_m8?si=fm6xDU2U0IdURKWJ" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

ARP works inside your local network to figure out which physical device is connected to which IP address. Every networked device has a MAC address—a unique identifier tied to its network hardware. When your computer wants to send data to another device on the same network, it knows the IP address but not the MAC address. ARP is used to ask, “Who has this IP?” and the device responds with its MAC address. That information is stored in a small table called the ARP cache, so the computer doesn’t have to ask again every time. ARP is essential for devices to talk to each other directly on a local network, but it's also a common target for attacks like ARP spoofing, where a hacker sends fake responses to mislead devices into sending data to the wrong place.


## TCP (Transmission Control Protocol)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/F27PLin3TV0?si=O_EDQA-mGGI7B_7i" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


TCP is a transport protocol that ensures reliable communication between two devices. When you load a website, send an email, or stream a video (depending on the service), TCP might be working in the background to make sure all the data gets delivered in the right order and without errors. It starts with a three-step process called the handshake (SYN, SYN-ACK, ACK) to establish a connection. After that, it keeps track of which packets were sent and received. If a packet is lost or arrives out of order, TCP handles resending and reordering it. This makes it perfect for applications where accuracy matters, like web browsing, file transfers, or secure remote access. Because of its extra checks and communication, it's a bit slower than other protocols, but much more reliable.



## UDP (User Datagram Protocol)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/jE_FcgpQ7Co?si=lgSaO4-3sXGcR7av" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

UDP is another transport protocol, but it’s much simpler and faster than TCP. It doesn’t establish a connection, doesn’t check if the packets arrive, and doesn’t resend them if they’re lost. It just sends the data and moves on. This makes UDP useful in situations where speed is more important than perfection—like in online games, voice or video calls, and streaming, where it’s better to lose a small bit of data than to slow everything down trying to fix it. Because of this, UDP has much less overhead than TCP and is often the go-to for real-time or low-latency applications.


## FTP (File Transfer Protocol)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/d5GrajJ8WMs?si=9n9XV_vrk0eI9zqy" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

FTP is a protocol used to transfer files between a client and a server over a network. It's one of the oldest internet protocols and works by creating two separate connections: one for commands (like login and file lists) and another for the actual file data. These typically use port 21 and port 20, respectively. FTP allows users to upload or download files from a remote system, but by default, it’s not secure—it sends usernames, passwords, and file data in plain text. There are secure versions like FTPS and SFTP (which is actually based on SSH), but traditional FTP is still found in many environments, especially during pentesting or in legacy systems.


## SMB (Server Message Block)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/csocwMe7l_E?si=2sOSDZRmvug5E-QL" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

SMB is a protocol mainly used by Windows systems to share files, printers, and other resources across a network. If you've ever accessed a shared folder on another computer, there's a good chance SMB was involved. It runs over port 445 and can either work with older systems using NetBIOS or directly over TCP. There are different versions—SMB1 is outdated and insecure, while SMB2 and SMB3 are much improved. SMB is a common target in security assessments because it’s often misconfigured or exposed unnecessarily, leading to vulnerabilities like the one exploited in the WannaCry ransomware attack.


## SSH (Secure Shell)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/5JvLV2-ngCI?si=tqoKGvwjbDp0E8BA" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

SSH is a secure way to remotely access another computer over a network, typically used by system administrators or developers. It encrypts everything you type and everything you receive, so attackers can’t see your password or commands even if they’re watching the network. SSH uses port 22 and supports both password and key-based authentication, with the latter being much safer. It has mostly replaced older tools like Telnet, which sent everything in plain text. SSH can also be used to securely copy files, tunnel other traffic, or automate remote tasks.


## HTTP and HTTPS (HyperText Transfer Protocol)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/wW2A5SZ3GkI?si=PxOfgVuMsurEJONE" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

HTTP is the protocol your browser uses to communicate with websites. It works over port 80 and follows a simple request-response pattern: your browser asks for a page, and the server sends it back. It’s stateless, meaning each request is independent—your browser has to include all necessary info each time. HTTPS is the secure version of HTTP and uses encryption (SSL/TLS) to protect the data being sent and received. It runs on port 443 and is what you see in the browser when there's a padlock icon. HTTPS ensures that passwords, personal info, and anything else you do on a site can’t be read by attackers watching the network.


## DNS (Domain Name System)
This protocol is very important and you need to understand it deeply , it may seem complex at first but just dig(wink) deep into it

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/NiQTs9DbtW4?si=nFOZFLXHar3nsMZg" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


DNS is like the phone book of the internet. It translates human-friendly domain names (like `rickross.com`) into IP addresses (like `93.184.216.34`) that computers use to talk to each other. When you visit a website, your device sends a DNS query to a DNS server to find the correct IP address. It uses UDP port 53 for normal lookups because it's fast, but it switches to TCP for larger responses like zone transfers. DNS is built in a hierarchy, starting from root servers, then top-level domains (.com, .net, etc.), and finally the authoritative servers that know about the specific domain.


## NFS (Network File System)

<div class="video-container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/k3RxOqftzsU?si=Qs_N-kDiA30FOzcd" 
          title="YouTube video player" frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

NFS is used mainly in Unix and Linux environments to let computers access files over a network as if they were on the local drive. This means you can mount a remote folder and open or edit files without copying them first. NFS makes networked storage seamless and efficient, especially in enterprise environments or labs. However, it’s often misconfigured—especially in CTFs and pentesting labs—where permissions are too loose or anonymous access is allowed, exposing sensitive files to attackers. NFS has several versions, each adding features and security improvements.

---

And with all those protocols and networks put togather by a stack(like TCP/IP) your waifu image traveled to you through the beautiful chaos of the internet, touching dozens of routers, switches, and servers, potentially getting sniffed by some script kiddie with Wireshark, but eventually making it to your screen in all its 4K glory.

![Foxy Plushy](https://media.tenor.com/hYkRcm80JFwAAAAi/foxy-foxplushy.gif)


There is more networking terms you can look up that you will need to understand like:

# General terms (i got tired of labeling)

## NAT (Network Address Translation)

NAT is a technique used by routers to allow multiple devices on a private network to share a single public IP address when accessing the internet. It works by translating the private IP addresses inside your home or office into one public IP address. When responses come back, NAT translates them back to the correct private device. This helps conserve IP addresses and adds a layer of security because devices inside the network aren’t directly visible to the internet.

## DMZ (Demilitarized Zone)

![dmz](/assets/img/Learning/dmz.png)

A DMZ is a small, isolated network zone placed between your internal network and the internet. It is designed to host public-facing services, such as web servers or email servers, so they can be accessed from the internet without exposing your entire private network. If a device in the DMZ is compromised, the attacker has limited access and cannot easily reach your internal, more secure network.


## VPN (Virtual Private Network)

A VPN creates a secure, encrypted connection (or “tunnel”) over the internet between your device and a remote network. This protects your data from being seen by others and allows you to access resources on the remote network as if you were physically there. People use VPNs to work remotely, protect their privacy, or bypass regional restrictions.


## Subnet

A subnet is a smaller segment of a larger network. It divides a big network into smaller parts to improve performance and security. Each subnet has its own range of IP addresses. Devices within a subnet communicate more directly with each other, while communication between subnets is managed by routers.


## MAC Address

A MAC address is a unique identifier assigned to a network device’s hardware (like a network card). Unlike IP addresses, which can change, a MAC address is fixed and helps devices identify each other on a local network.




byebye 😘
