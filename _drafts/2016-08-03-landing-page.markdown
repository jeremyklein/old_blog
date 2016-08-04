---
layout: post
title:  "Hosting a landing page"
date:   2016-08-03 19:33:00 -0400
categories: Landing-Page
---

It seems like every developer worth their salt has a landing page with their name on it. I decided to take the quick and dirty approach of using a Digital Ocean droplet to serve a static page I spun up using Bootstrap.

# Step 1 Buying the domain

This step can be as easy as heading over to one of the big domain name registrars and wiping out your credit card. 

If you are the kind of person who's partial to tinfoil hats, and worried that the registrars are engaging in [Domain Name Frontrunning](https://en.wikipedia.org/wiki/Domain_name_front_running) finding out if a domain is available is doable from the command line. 

For example, to check if google.com is available just execute the following command:

	Whois google.com

 Step 2 Creating a Digital Ocean Droplet

 Digital Ocean is a service that makes it dead simple to spin up a VPS. With a few clicks, a couple minutes, and $5 a month, I had a private server with Ubuntu 16.04 Shiny set up. a few recommended steps 

 1. [setting up ssh keys](https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-freebsd-server)
 2. [adding user adding ssh disable ssh to root user](https://www.evernote.com/Home.action#n=6ffe7aa0-f811-4280-8167-26ef0d7da0bc&ses=4&sh=2&sds=5&)

 Step 3 Setting up Apache to serve my static Bootstrap page

 1. [setting up apache](https://www.atlantic.net/community/howto/install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04/)



 Step 4 Configuring UFW

 1. [configuring UFW](https://www.digitalocean.com/community/tutorials/how-to-setup-a-firewall-with-ufw-on-an-ubuntu-and-debian-cloud-server)

 Step 5 Configuring SSL

 [certbot](https://www.evernote.com/Home.action#n=ecb8bd14-2eb7-4375-8456-a96196537221&ses=4&sh=2&sds=5&)
 [cron](https://www.evernote.com/Home.action#n=d5c00b22-3287-4044-9bc5-c2ca9ce56234&ses=4&sh=2&sds=5&)

 Step 6 Redirect traffic from 80 to 443

	 In sites enabled, Redirect permanent / https://jklein.co

 Step 5 Adding Record to DNS

 [adding Record to DNS](http://withr.me/add-domain-name-for-your-server-on-digitalocean/)