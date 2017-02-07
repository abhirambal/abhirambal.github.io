---
layout: page
title: Projects/Research
---

 - ### Fast NVMe layer for a decomposed kernel (Master thesis)

	Operating system (OS) kernel extensions, particularly device drivers, are one of the main sources of
	vulnerabilities in the commodity OS kernels widely used today. This is mainly because of bugs that are
	routinely introduced in the driver code due to rapid development rate and fast changing device config-
	urations. Vulnerabilities in driver code are often exploited by attackers that lead to privilege escalations,
	DoS attacks, arbitrary code execution, etc. Today, kernel extensions are fully trusted and operate within
	the core kernel without any form of isolation for better performance. But history suggests that this trust is
	misplaced. As the security of many applications depend on the kernel to be secure, it becomes extremely
	important to introduce some form of isolation to contain the effects of a vulnerable driver code.
	We develop a new framework for isolating device drivers in the Linux kernel. 

	Our work builds on
	three key principles (1) strong isolation of driver code, (2) transparency for existing source (with no or
	minimal changes to the source), and (3) same or better performance compared to the non-isolated driver.
	Compared to existing device driver isolation techniques (device driver virtual machines, and clean-slate
	user-level device driver implementations), our work remains transparent to the existing device driver
	code, and implements a lean I/O path without introducing overheads of full-system virtualization. We
	demonstrate our approach by isolating the NVMe (Non-Volatile Memory Express) driver in the Linux
	kernel.

 - ### Software fault isolation framework in Rust (During my internship at Samsung Research America)
	The main idea of the work was to utilize the safe features of Rust programming language for systems programming.

	Built a protection domain library to support fault isolation using the safe features of Rust,
	extended [NetBricks](https://github.com/NetSys/NetBricks) with the protection domain library to contain faults.
	Also implemented recovery mechanism and automatic checkpointing of objects.

	Submitted for HotOS XVI

 - ### Mitigating SROP (Sigreturn Oriented Programming) attacks in Linux Kernel 
   	SROP is a new kind of attack wherein, the attacker exploits the signal handling framework of the kernel. 
	In Sigreturn Oriented Programming, an attacker causes a user-space program to call the sigreturn system call in order 
	to get complete control control over the entire userspace context in one go. This attack is special in the sense that 
	an attacker can coax any value into the registers they please by using SROP. 
	Previously, an attacker would have to search for ROP gadgets to do this but now it can be accomplished with one sigreturn.

	See [here](http://www.cs.vu.nl/~herbertb/papers/srop_sp14.pdf) for more information and the patch set [here](https://lkml.org/lkml/2016/2/6/166)
