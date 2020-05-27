---
layout: page
title: HPC RSE Meeting Notes: 26 May 2020
summary:
---

# HPC RSE Meeting Notes: 26 May 2020

28 Attendees

## Actions

  - (AndyT/JamesG) Look at organising online event to bring workflow tool developers together with
    HPC RSEs to explore the space and how these tools can be enabled in MFA world.
  - (AndyT) Propose SocRSE online event on online training this year to SocRSE trustees
    - Proposed, will see what happens
    - CarpentryCon@Home will also be covering this (see below for deatils)
  - (AndyT) Suggest that ExCALIBUR run a webinar to bring community up to date with the project
    - Scheduled for 1100 BST, 10 June 2020: [https://www.archer2.ac.uk/training/courses/200610-excalibur/](https://www.archer2.ac.uk/training/courses/200610-excalibur/)

## Topics of interest

### Security on HPC systems

  - MFA introduction
    + Is 2FA an overkill response here? It may cause too much pain and stymie research?
    + It seems a reasonable response to limit lateral movement of attacks from one compromised system to another system given that many researchers have accounts on multiple systems
    + Already widely used on US HPC facilities
  - MFA issues for research workflows
    + More complex frameworks: Ansible, AiiDA, FireWorks
    + Large data transfers
    + In all of these cases you want to re-use the SSH connection without re-authenticating each time
      * Often used SSH Agents to enable this - will not be possible in the same way using MFA
  - Potential workarounds
    + SSH multiplexing: e.g. [https://en.wikibooks.org/wiki/OpenSSH/Cookbook/Multiplexing](https://en.wikibooks.org/wiki/OpenSSH/Cookbook/Multiplexing)
    + SSH proxies: e.g. [https://docs.nersc.gov/connect/mfa/#sshproxy](https://docs.nersc.gov/connect/mfa/#sshproxy)
    + Host workflow nodes within the security perimeter of HPC system: [https://docs.nersc.gov/jobs/workflow/workflow_nodes/](https://docs.nersc.gov/jobs/workflow/workflow_nodes/)

  - Other potential options
    - JISC Assent - federated credentials: [https://www.jisc.ac.uk/assent](https://www.jisc.ac.uk/assent)
    - Google BeyondCorp - secure in a different way: [https://beyondcorp.com/](https://beyondcorp.com/)
    - SSH certificates: e.g. [https://smallstep.com/blog/use-ssh-certificates/](https://smallstep.com/blog/use-ssh-certificates/)
    - Would be useful to have an event to discuss these options - maybe more in the HPC-SIG space rather than the HPC RSE space

## National HPC RSE Updates

### ARCHER/ARCHER2/Cirrus/DiRAC, EPCC

  - Most systems have been down due to the recent security incident
  - Developing new training for ARCHER2 but could be re-used for other sites if they are interested
    - [https://github.com/EPCCed/archer2-intro-package](https://github.com/EPCCed/archer2-intro-package) (mostly complete)
    - [https://github.com/EPCCed/archer2-intro-develop](https://github.com/EPCCed/archer2-intro-develop) (still in development)
  - Investigated pros and cons of EasyBuild vs Spack for research software management
    - Webinar at 1500 BST on 17 June 2020: [https://www.archer2.ac.uk/training/courses/200617-spack-easybuild/](https://www.archer2.ac.uk/training/courses/200617-spack-easybuild/)
    - Plan to publish report
  - 1st ARCHER2 eCSE Call is open: [https://www.archer2.ac.uk/ecse/](https://www.archer2.ac.uk/ecse/)

### Isambard, GW4

  - Isambard was taken offline due to the incident. 
    - No evidence of access/escalation
    - Continued to churn through jobs until Wednesday morning when straggling jobs were purged and patching began
    - ARM component returned to service with scrambled passwords and forced ssh key changes as per ARCHER advice
    - These have to be updated manually
    - ‘MACS’ resistant to change remain offline while patching completed
 
  - Developed security page for Intro to HPC/HPC Carpentry, appears to have developed into a workshop lesson in
    its own right:
    + [https://arc-lessons.github.io/security/00_schedule.html](https://arc-lessons.github.io/security/00_schedule.html), repo: [https://github.com/arc-lessons/security](https://github.com/arc-lessons/security) issues PR welcome.

## Upcoming training, events and meetings

  - ARCHER2 Training: [https://www.archer2.ac.uk/training/#upcoming-training](https://www.archer2.ac.uk/training/#upcoming-training)
    + ARCHER2 eCSE Webinar Wednesday 27th May 2020 15:00 - 16:00 BST
    + ARCHER2 Outreach webinar, Online, Wednesday 3rd June 2020 15:00 - 16:00 BST
    + ExCALIBUR - an algorithmic approach to exascale design, webinar, Online, Wednesday 10th June 2020, 11:00 - 12:00 BST
    + Software Packages in HPC with Spack and EasyBuild webinar, Online, Wednesday 17th June 2020 15:00 - 16:00 BST
  - [CarpentryCon@Home](https://carpentries.org/blog/2020/05/2020-carpentrycon-at-home-proposals/)

## Date of next meeting

1400 UK Time, TBC June 2020
