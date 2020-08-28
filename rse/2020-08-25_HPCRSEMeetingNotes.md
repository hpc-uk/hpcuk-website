---
layout: page
title: HPC RSE Meeting Notes, 25 August 2020
summary:
---

# HPC RSE Meeting Notes: 25 August 2020

18 Attendees

## Actions

  - (AndyT/JamesG) Look at organising online event to bring workflow tool developers together with HPC RSEs to explore the space and how these tools can be enabled in MFA world.
    - Maybe look at one of the SORSE events for this
    - IRIS looking at command line access via federated access (via STFC)
  - (AndyT) Raise option of authentication workshop with HPC-SIG
  - (AndyT) Organise presentation on IRIS authentication work to this group

## Topics of interest

### Modules

#### Do sites prefer TCL or Lmod? Why?

  - Most people seem to have a preference for Lmod
  - Perceived advantages of Lmod over TCL:
    + Lmod has a richer feature set
    + Better handling of conflicts and dependencies
    + More intelligent loading of different features
    + Substring search on module names
    + Modulefiles can be written in either TCL or Lua - allows for easier transition to Lmod from TCL
  - Perceived disadvantages:
    + Lmod can be "too clever" and hide the full set of software available for power users
  - However, though people like Lmod better, most people still use TCL on their systems
    - Many systems come with this preinstalled by the vendor
    - Can be difficult to change in mid-service: have to reeducate users and change all the documentation
    - For Cray systems, you are currently tied into TCL due to their programming environment though they plan to offer Lmod as an option later this year

#### How do different sites organise their modules - hierarchical, flat?

  - Lmod makes this easier as you can use advanced features to allow for different options (e.g. *families*)
    - Recent TCL has *flavours* which are similar to Lmod families
  - Hierarchical arrangement can make it more difficult for people to select the right configuration and to search for modules in TCL
    + Some people have used an inverted heirarchy, e.g. `fftw/gcc9/ompi4/3.3.4.8` rather than `gcc9/ompi4/fftw/3.3.4.8` as this helps with searching in TCL
  - Flat can help for module discovery and make it easier to select the configuration you want
  - Might be good to be able to load application and then hide all the incompatible stuff so you only see modules relevant to the environment you currently have
  - Could potentially have two different views - heirarchical or flat depending on the user preference
    + EasyBuild can redo a build and only generate modulefile (without recompile) to give you a different view in an automated way
    + Could be be easy to with Spack too but may need some simple coding to enable this

#### Can user groups contribute their own modulefiles? If so, how is this managed?

  - UCL: Groups can ask for space to install software and then request the addition of modulefiles by the service
  - Ghent get users to contribute working EasyConfiggs that they can then use to provide software/modules centrally
  - ARCHER2 has plans to make this available and ensure that they distinguish between modules/software supported by service and those provided by users

#### Example configurations

Some sites have started publishing their configuration to allow others to build on them:

  - https://github.com/ComputeCanada/software-stack-config/tree/master/lmod
  - https://github.com/hpcugent/Lmod-UGent

## National HPC RSE Updates

### EPCC: ARCHER, ARCHER2, Cirrus, DiRAC Extreme Scaling

  - ARCHER2
    - Porting and testing on ARCHER2 Test and Development System (TDS) based in Cray factory in US continues
    - Webinar next week on early experiences: https://www.archer2.ac.uk/training/courses/200902-archer2-tds/ 
    - Initial 4 cabinets of ARCHER2 have arrived at EPCC and HPE Cray are working to install latest Shasta system software before handing over to EPCC for commissioning
    - Continued to develop documentation at: https://docs.archer2.ac.uk
    - Initial introductory courses for the new system developed and tested
    - Large number of TAs evaluated for the EPSRC Access to HPC call
  - Cirrus
    - Various upgrades to improve the system - tuning of scheduler setup, additional pieces of software
    - Continuing to develop and improve documentation
    - Large number of TAs evaluated for the EPSRC Access to HPC call
  
### NI-HPC

  - The NI-HPC tier2 hardware is now installed running.
  - We opened the system to all QUB & Ulster users on 28th July.
  - Since 1st July there have been ~27K jobs run.

  - The two new RSEs (who attended the Aug RSE meeting) are getting up-to-speed and supporting the exemplar areas.
  - One has been working on running Neuroscience MATLAB programs
    - He is also tasked to do a 1hr "running MATLAB on kelvin2" lecture on 25th September. (maybe others may be interested?)
    - On training, we are putting together some GPU training for Dec/Jan.
    - He has onboarded 20 Ulster researchers onto kelvin2 to date.
  - Second has been trying to get NAMD to run - still ongoing.
    - Has also been testing software against updated drivers on one of the GPU nodes - needed for adding CUDA 11.

  - We have added jupyter notebooks to kelvin2.

  - The NI-HPC website ready to publish internally and have applied for ni-hpc-ac.uk domain name.

### GW4 Isambard

#### Presently

Isambard is well used, with utilisation over 90%. On the one hand this is positive as it shows the community are making use of ARM at scale, on the other hand this has led to an increase in queue wait times. In response we are increasing our monitoring of the queues and changing the fairshare scheduling to ensure the RAP projects get access to the resource they need in the time they have. 

We are beginning the process of feeding back the usage statistics from Isambard to SAFE so that PIs can see their usage against their allocations.

In terms of follow-up from the security incident earlier this year, we haven't made any changes to authentication methods this month. In last month's call it was decided that this group isn't the proper venue for taking that forward, so James Davenport from Bath is speaking with the RUGRIT lead on response to incident, around learning and review of authentication methods (and coordinating changes) and Simon McIntosh-Smith from Bristol is doing similarly with Tier2 Technical directors. 

This month we we have made a push to improve our online documentation, identifying areas for improvement and development.

#### Upcoming

As part of the Isambard 2 project the current system will be doubled by the addition of a second XC50 cabinet with approx 10 000 ARM cores using same Marvell ThunderX2 CPUs as the existing ones. According to the vendors this update is still on track in terms of shipping and installation and should be available to users later.

Even more excitingly we are still on track for the shipping and installation of a number of A64FX nodes (the same ARM based processors used in the Top500 number 1 system Fugaku). Once those are installed and working satisfactorily we aim to have one or more "hackathons" as we did for the initial Isambard system for developers to port and test their codes on that architecture.

### MMM Hub

Young (previously referred to as Thomas 2) has finished its initial pilot phase, and will be going into service for an extended open pilot for the partner institutions until October, when resource allocation will begin.

We did our first trial run of HPC Carpentry on 27 and 28 July, two half days. On the whole it went well, though not helped by a major datacentre incident on day 2! We are planning to make it three half days next time, to make it less rushed. (Ran it using Blackboard Collaborate since UCL has it).

## Upcoming training, events and meetings

  - The Sandia labs people are continuing their Kokkos lecture series (friday afternoons UK time)  https://github.com/kokkos/kokkos-tutorials/wiki/Kokkos-Lecture-Series
  - SYCL are running their Summer sessions 4-5pm August 31st–September 4th, 2020 https://ti.to/sycl-summer-sessions/sycl-summer-sessions-2020
  - Relevant SC20 sessions
  - Women in HPC https://womeninhpc.org/events/sc20/workshop
  - Research Software Engineers in HPC (RSE-HPC-2020) https://us-rse.org/rse-hpc-2020/

  - CIUK 2020 is going virtual https://www.scd.stfc.ac.uk/Pages/CIUK2020.aspx* 

  - IEEE Cluster2020, 14-17 September, online (free registration): https://clustercomp.org/2020/

  - Hoping to run an HPC Champions meeting next month. Likely 2 half days 17th/18th September, through the SORSE series. Look out for more info by the end of the month including a call for talks

## Date of next meeting

1400 UK Time, TBC September 2020
