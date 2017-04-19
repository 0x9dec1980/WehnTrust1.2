# Who wrote WehnTrust

All credit goes to the original developers, not me. This is just a backup of the code of WehnTrust before CodePlex shutting down.

Original website: http://wehntrust.codeplex.com/
Original devs: skape, wag, http://wehntrust.codeplex.com/team/view

The rest of the README is information taken from the original website.

# Overview

WehnTrust is a Host-based Intrusion Prevention System (HIPS) for Windows 2000, XP, and Server 2003. It includes support for exploit mitigations that are designed to make exploitation more difficult by preventing the use of specific exploitation techniques and by making exploitation unreliable.

# How it works

WehnTrust randomizes the base addresses of memory allocations to make it more difficult to exploit software vulnerabilities such as buffer overflows. This technique is commonly known as Address Space Layout Randomization (ASLR) and was originally conceived by the PaX team. Microsoft has recently incorporated support for ASLR into Windows Vista and Windows Server 2008. In addition to ASLR, WehnTrust generically mitigates SEH overwrites by dynamically validating a thread's exception handler chain prior to allowing exceptions to be dispatched. 

# Recommendations

Using WehnTrust in combination with hardware-enforced DEP (non-executable pages) as included with Windows XP SP2 and Windows Server 2003 provides the greatest level of security. Non-executable pages help to counter some of the inherent weaknesses of ASLR.

# Features

The following features are included:
Address Space Layout Randomization (ASLR)
Randomized image file mappings (relocations required)
Randomized memory allocations (e.g. VirtualAlloc)
Randomized PEB/TEB
Basic brute force detection and prevention
SEH Overwrite Prevention
Format string vulnerability prevention
Logging and notification of exploitation attempts
Balloon tip nofication
Native windows event logging
Application and image file exemptions

# License

WehnTrust is licensed under the WehnTrust Software License 1.0.

# Thanks

We would like to thank the following people for sharing their knowledge, help, and support during the development of WehnTrust: the PaX team, Erik Cabetas, Richard Johnson, HD Moore, Patrick Stach, Jarkko Turkulainen , Martin Zeiser.



