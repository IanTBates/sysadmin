# Docker Project

#### Install

```
sudo apt update
sudo apt install docker.io
```
```
sudo service docker status
```
If not already active, then start docker with

```
sudo service docker start
```

What follows is something that might have to be done?
```
sudo apt update
sudo apt install docker-compose-plugin
```
![Alt text](image.png)

It failed, just moving on, for now.
*it failing had no effect.

## Adventure #1
### Install OpenVAS/Greenbone vulnerability scanner via Docker

https://github.com/mikesplain/openvas-docker

#I followed the video guide, which uses this github to download a container for openvas. 

This github page contains lists of commands and references for docker containization.

```
sudo docker run -d -p 443:443 --name openvas mikesplain/openvas
```
![Alt text](image-1.png)

Run with sudo.

![Alt text](image-2.png)

Then wait.

![Alt text](image-3.png)

Then check your CPU usage for complete download of signatures.

![Alt text](image-4.png)

![Alt text](image-5.png)

The CPUs have settled down.

I may need to add more RAM to the VM later.

![Alt text](image-6.png)

Accept the risk and continue.

![Alt text](image-7.png)

Log in using "admin" for both username and password. 

![Alt text](image-8.png)

![Alt text](image-9.png)

I used the wizard, default.

Oh boy is it slow.

Definitely assigning more ram and CPUs.

![Alt text](image-10.png)

The results of the scan show 2 issues.

I am now going to scan my own defualt gateway.

![Alt text](image-11.png)

So, my home network is missing the 'secure' Cookie attribute.

# Thats all