Basic Kernel Issue Resolution, A Disclaimer, and Why I Wrote This Book
======================================================================
.Sdrawkcab nettirw si retpach siht

Why I Am Writing This Book
--------------------------
I installed my first Linux distribution when I was about 13 years old on a
Compaq Presario with a purple, curved faceplate. Back then, if you had an issue
during installation, there were few automatic, user-friendly ways of fixing
those issues and you had 2 choices, try a different distribution or resolve it
yourself. The first one I got to work was Slackware, and it didn't work
entirely the first time around. I spent weeks on my Windows partition copying 
things I thought might help me resolve my issue(a malfunctioning desktop window
manager). This sort of rite-of-passage is typical of alot of people in my 
generation of GNU+Linux enthusiasts, we started out hoping to be users but found
the kind of freedom we could have with our hardware by working through an issue
we had with it on a system that would allow us to do so. Thousands of man-hours
of fixes contributed have given us highly user-friendly distributions like 
Ubuntu and Android, general-purpose base distributions like Fedora, Debian, and
Arch, highly secure Linux distributions like Alpine and penetration testing
Distributions like Kali Linux. Even SteamOS can use Linux as it's basis. These
days, they *all work great* and that's largely a function of transparency and
the involvement of tech industry workers, academics, and enthusiasts getting
involved with their development. Eventually, a lot of us learned from [Linux From Scratch](https://linuxfromscratch.org)
\(Which is still an active and excellent resource which will be very helpful as
you port AOSP, CyanogenMod, Replicant, etc to your device\)how Linux systems 
were put together, and we learned to code, then we learned to code better, and 
administer software, and all kinds of cool stuff. It's in that spirit of Free 
Software, personal freedom, and ownership that this book is written. There are
hundreds of millions of potential enthusiasts who could extend the hardware and
upstream support of the billions of devices produced and sold each year. These 
tiny computers, in the pockets of thousansds of people all over the world, are
discarded every day when they could be repurposed into everything from massive
parallel computing clusters, industrial control systems, robot brains, or even
used in conjunction with a keyboard and mouse as a workstation computer for
somebody who just wants to get a better job. This an attempt to empower and 
stimulate new business and innovation, and most of all indiviuals. It can also
have other side-effects, like potentially reducing e-waste and the consequent
poisoning and victimization of the environment and citizens of industrially
undeveloped countries. I encourage you, in spite of the difficulties I am about
to outline, to nonetheless persevere in your own efforts to port to your device
and consider all the possibilities that go even beyond the amazing functionality
of a modern phone.

And Now, the Disclaimer
-----------------------
There are two chapters in this book that can brick your device. This is one of
them. 

Here's the deal. This bit deals with fixing up your device for use with a 
different Linux kernel than the one supplied by the manufacturer. The best
reason for this is in order to backport a newer userland\(say, Android 4.4\) to
a device which previously used an older Kernel\(Say, Linux 3.0.8, used on 
Android 4.0.4\) Sometimes, it's easy because the **upstream support** for a
device's hardware is good. Upstream Support means that the hardware in a device
is officially supported in the Linux Kernel. Unfortunately, unless it's
particularly well supported, it might be pretty hard to figure out whether a
device has hardware with upstream support, and it might be hard to figure out
what options you need to enable in a new Kernel defconfig in order to use that
hardware. And that's before you even get to the part where you have to compile
the kernel and deal with the sections of the code which don't work because of
some peculiarity of your system. And while it's not *likely*, a mistake in this
process can *potentially* make your device unfixable. And there's good news, you
can even usually recover from a bad flash. Like, 95% of the time, you're not
going to wind up with an unfixable device.

So go carefully forward.

And one final note, please write documentation and put it online somewhere.

Without Further Ado
-------------------
