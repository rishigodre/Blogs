# I hope you are now convinced to start a homelab, so now lets go to the potatoes and gravy

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
Ok so kids for this lecture we learned how to homelab. Next we will learn about my setup. No AI was used to write this so if it is $#!T it is purely my fault.
