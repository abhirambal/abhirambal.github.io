---
layout: page
title: Projects
---

## Current

 - ### Mitigating SROP (Sigreturn Oriented Programming) attacks in Linux Kernel 
   SROP is a new kind of attack wherein, the attacker exploits the signal handling framework of the kernel. In Sigreturn Oriented Programming, an attacker causes a user-space program to call the sigreturn system call in order to get complete control control over the entire userspace context in one go. This attack is special in the sense that an attacker can coax any value into the registers they please by using SROP. Previously, an attacker would have to search for ROP gadgets to do this but now it can be accomplished with one sigreturn.

   See [here](http://www.cs.vu.nl/~herbertb/papers/srop_sp14.pdf) for more information.
   
   Credits to [Scotty](http://www.eng.utah.edu/~sbauer/) for implementing the idea and upstreaming it to mainline. See [here](https://lkml.org/lkml/2016/2/6/166) for the patch set.

