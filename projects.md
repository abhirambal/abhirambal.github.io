---
layout: page
title: Projects/Research
---

 - ### Towards a fast NVMe layer for a decomposed kernel ([Master Thesis](http://abhirambal.github.io/Thesis_final_u1009804.pdf))
	Operating system (OS) kernel extensions, particularly device drivers, are one of the primary sources of 
	vulnerabilities in commodity OS kernels. Vulnerabilities in driver code are often exploited by attackers, 
	leading to attacks like privilege escalation, denial-of-service, and arbitrary code execution. 
	Today, kernel extensions are fully trusted and operate within the core kernel without any form of isolation. 
	But history suggests that this trust is often misplaced, emphasizing a need for some isolation in the kernel.
	We develop a new framework for isolating device drivers in the Linux kernel. Our work builds on three fundamental 
	principles: (1) strong isolation of the driver code; (2) reuse of existing driver while making no or minimal changes 
	to the source; and (3) achieving same or better performance compared to the nonisolated driver. In comparison to
	existing driver isolation schemes like driver virtual machines and user-level device driver implementations, our work 
	strives to avoid modifying existing code and implements an I/O path without incurring substantial performance overhead.
	
	We demonstrate our approach by isolating a unmodified driver for a null block device in the Linux kernel, achieving near-native 
	throughput for block sizes ranging from 512B to 256KB and outperforming the nonisolated driver for block sizes of 1MB and higher.

 - ### Software fault isolation framework in Rust (During my internship at Samsung Research America)
	The main idea of the work was to utilize the safe features of Rust programming language for systems programming.

	Built a protection domain library to support fault isolation using the safe features of Rust,
	extended [NetBricks](https://github.com/NetSys/NetBricks) with the protection domain library to contain faults.
	Also implemented recovery mechanism and automatic checkpointing of objects.

	Related reading:
		1. See [publications](http://abhirambal.github.io/publications/)
		2. [Morning paper's discussion](https://blog.acolyer.org/2017/06/14/system-programming-in-rust-beyond-safety/) 

 - ### Mitigating SROP (Sigreturn Oriented Programming) attacks in Linux Kernel 
	
	SROP is a new kind of attack wherein, the attacker exploits the signal handling framework of the kernel. 
	In Sigreturn Oriented Programming, an attacker causes a user-space program to call the sigreturn system call in order 
	to get complete control control over the entire userspace context in one go. This attack is special in the sense that 
	an attacker can coax any value into the registers they please by using SROP. 
	Previously, an attacker would have to search for ROP gadgets to do this but now it can be accomplished with one sigreturn.

	See [here](http://www.cs.vu.nl/~herbertb/papers/srop_sp14.pdf) for more information and the patch set [here](https://lkml.org/lkml/2016/2/6/166)

 - ### Patches to Linux Kernel
	- [Standard Deviation bug](https://git.kernel.org/pub/scm/linux/kernel/git/stable/stable-queue.git/tree/queue-4.11/staging-iio-tsl2x7x_core-fix-standard-deviation-calculation.patch?id=8f717a5ca7b61c0685645caf62f4589310954c7b)
