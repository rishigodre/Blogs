# How to Homelab: for beginners by beginner

## What is a home?lab???
I get it, random 2 words joined together make no sense. Home because it is in your home like you own it, no corporate subscription magic (duhhhhhhh), and lab coz it is a place to experiment and bring to life your dream of owning a server or many. But but but "what is a server?" your ask, it is just a computer, yes that unassuming black or if you are vintage then beige box that sometimes does not start so you hit it a few times and it starts working connected to the internet and serves traffic or stores data for you, so just a computer with a lot of internet. This will allow you to bring in house or on-prem if you fancy all the software servcies you rely on day to day. Google photos, gone; cloud storage, gone; your privacy and security (you think I will say gone ? really ??) no gain back. Whatever runs on a server or even serverless you can run in your lab.

## Firstly lets get the WHY out the way
Why spend money, time, and energy trying to do something that is already a few clicks and an autopay away. Privacy, Freedom, Control, and Learning, just kidding we all do it because we want to sound cool (I have a homelab BTW), or have watched one too many LTT videos, or simply love pain (I tried installing linux on a system with a decade old Nvidia card, I know what pain is). 

### Privacy
I created an Instagram account in 2021 thinking it will be my digital album and did post a lot of pics on it, but my personal photos being used to train AI and the terms are yes by default is unacceptable. I don't want my face to appear in some AI goon slop or more likely in some AI slop India hate post on X.
My pictures and videos not leaving my home and the ability to view them anywhere is awesome. Free from all the tracker of the interwebs watching how fast you type to determine your mood and sell you stuff accordingly. 

### Freedom and Control
Want service A over B, go for it. Want to delete everything and start over, more power to you. Want to make something that does not exist but you have the drive to make it, there is a whole community that will help you out. Want to obtain all the 300TB of linux ISOs that got leaked from spotify (Don't worry Trillion/Billion Dollar companies do it and don't get into any trouble why will you ?). Pure red white and blue freedom (lol).

### Learning
As a Developer, Sys admin, Network engineer, or just a tinkerer, there is a lot to learn about each of these fields for a homelab. Linux, Docker, Kubernetes, Bulbasaur, Charmander, Squirtle, NFS, ISCSI, RAID, ZFS, SMART, ACL, IP, HTTP, SSL, tunnels, LXC, VM, DNS, and a lot lot more (Also how expensive this hobby can get). This knowledge is very useful when you get into the real world and you get to tell your colleagues about how awesome your homelab is (really rub it in their faces till they start avoiding you so you have more time to pretend as a sys-admin).

## Cost - I know it is very important for us
Old computer, new drives - GO. CPU, RAM, Motor board, Power supply, and case don't degrade, storage does. 10 y/o computer with a SSD to boot and some drives for storage is good to go. So the question still stands how much does all this cost, IT DEPENDS currently the PC hardware market is very volatile unlike the usual where it is very stable, so for 15k you should be good to go with 512GB to boot and a few TB of mirrored storage.

## Do you really need it:
You yes you right now sitting on the bowl, you love ADs right, those unskippable 1 min ads that make sure you learn about AI tools for just ₹5 from a sus guy, yes so the homelab will take away this love of yours. The peace of mind that I have knowing my childhood pictures are not in my dads old dying CD/DVD collection or some 10 y/o drive but in my crappy server that is running 24/7 is immense (3-2-1 data backup is highly recommended). Recovering old media and seeing people enjoy it is all worth it. I want to show my children my childhood pictures. I am not into movie watching but watching 4k blue-ray quality with 5.1 surround will spoil you. The best part of all this is that everything here is automated and requires setup and nothing else.

#### I hope you are now convinced to start a homelab, so now lets go to the potatoes and gravy

## Things you absolutely can't bargain
1. Document and Plan - the first and most ignored part (My server has been up for 6 months at the time of writing this, so I am guilty as well). But make a list of all the random computer bits you have and have bought, and think about all the things you plan to do and how you will achieve them. Making a solid plan is a must as it will help you plan your capacity and buy hardware. Watch some youtube tutorials or read some blogs (such as mine) to get insights about how to do it.

2. WIRED CONNECTION TO YOUR SERVER - networking over wifi is absolutely $#!T and will make your life 1000000 times difficult + you don't want your server to hog all the bandwidth of your poor router + access point + switch (Mom wants to watch her daily soaps, and if it buffers then human technology has not advanced enough according to her). Further some OSs such as TrueNAS remove the wireless driver entirely. ["Avoid using WLAN if possible"](https://pve.proxmox.com/wiki/WLAN), are the first words of proxmox wiki on WLAN (Wifi). So make sure your server has a wired connection (It wants to feel like a real server even though it is a Dell nugget). 

3. Check the specs and manuals - yes I said it, read the manual there is no shame in not having your cpu and motherboard blow up because you connected the wrong cables together (In this economy you can not afford such fireworks). Buy the correct type of cable for your ethernet, SATA, SAS (if you have it). These are relatively cheap components so don't be penny wise and pound foolish.

4. Overspec if you can - this opens up avenues for upgrades down the line or unexpected capacity requirements or component failure. Even if you have to stretch the budget a little (buy once cry once). Having extra RAM never hurts anyone.

5. Have an iGPU in the CPU - not having one forces you to use a discrete graphics card which if it is an nvidia card will never work first try and you will have sleepless nights trying to figure out why your install is failing also there is no point in increasing your power usage for just a video output.

6. You do not need a monitor running all the time - The box thing is the computer, everything else is optional after installation so don't worry you won't need a screen attached to your server/s all the time.

7. Get comfortable with Linux and Terminal - Ahhhhhhhhhhhhhh!!!!!! noooooooooooooooo it is soooo scaryyyyy, shut up it is not that difficult. The way I like to go about it is that think of the action you want done (I know you want to run javascript on it already), now search how to do so and so in linux (search with distro name even better) using the terminal. Ever though that instead of searching you could ask the people who made something how to use it ?, Dumbo those are called the official docs and they are your best friends embrace them.

8. OverProvision!! - For example you have 6 physical cpu cores on your cpu (find it out using the part number of your cpu) you are not limited to say 3 VMs of 2 cores each, or 2 VMs of 3 cores each, you can go mad with the allocation make 10 VMs of 4 cores each just make sure that when a VM expects a core to be available it has some compute power to itself. This is a normal practice in Data Centers so nothing to worry about here.

9. Other important stuff - UPS, other copies of data you don't wish to loose (3-2-1 rule of data backup), RAID, minimize any single points of failure. Remember 2 is 1 and 1 is none. And don't forget to love the process.

## STOPPP NOW! 
Ok so kids for this lecture we learned why you need a homelab and how to start. Next we will learn about my setup. No AI was used to write this so if it is $#!T it is purely my fault.
