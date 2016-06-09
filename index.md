---
layout: page
---

<div style="width: 100%; display: inline-block;">
<img src="{{ site.baseurl }}/public/AB.jpg" alt="Headshot" width="25%" style="float: left;"/>
<div style="float: left; padding-left: 20px;">
<span style="font-size: 150%;">Abhiram Balasubramanian</span><br>
CS Graduate Student<br>
University of Utah<br>
<a href="mailto:abhiram@cs.utah.edu">abhiram@cs.utah.edu</a>
</div>
</div>

<p></p>

[Projects](#projects) -
[Hobbies](#hobbies) -
[Blog](./blog/)

I often go by the moniker AB (or) sometimes Abi as people find it much easier to call me that way.

I am an aspiring computer scientist, pursuing masters in Computer Science at the [School of Computing](www.cs.utah.edu), as keen as mustard about low-level kernel hacking, systems programming and hard-real time embedded system design.

I am also a Graduate Research Assistant and I work with Professor [Anton Burtsev](https://www.cs.utah.edu/~aburtsev) in [XCap](https://flux.utah.edu/project/xcap) project.

Previously, I was employed with [Robert Bosch Engineering and Business Solutions](http://www.bosch-india-software.com/en/homepage/rbei_homepage.html) as a Senior Software Engineer where I worked for the Linux-internal Center of Competence close to 2 years. Prior to that, I started my career at an embedded systems startup company where I worked for [BnR automation Gmbh](http://www.br-automation.com/en-us/perfection-in-automation/) close to around 2.5 years.
 

# <a name="projects"></a> Projects

## Current

 - Mitigating SROP (Sigreturn Oriented Programming) attacks in Linux Kernel
   SROP is a new kind of attack wherein, the attacker exploits the signal handling framework of the kernel. In Sigreturn Oriented Programming, an attacker causes a user-space program to call the sigreturn system call in order to get complete control control over the entire userspace context in one go. This attack is special in the sense that an attacker can coax any value into the registers they please by using SROP. Previously, an attacker would have to search for ROP gadgets to do this but now it can be accomplished with one sigreturn,

   See [here](http://www.cs.vu.nl/~herbertb/papers/srop_sp14.pdf) for more information.
   
   Credits to [Scotty](http://www.eng.utah.edu/~sbauer/) for implementing the idea and upstreaming it to mainline. See [here](https://lkml.org/lkml/2016/2/6/166) for the patch set.


# <a name="activities"></a> Hobbies

 - Photography
