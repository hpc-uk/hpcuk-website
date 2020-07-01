---
layout: page
title: HPC RSE Meeting Notes: 30 June 2020
summary:
---

# HPC RSE Meeting Notes: 30 June 2020

17 Attendees

## Actions

  - (AndyT/JamesG) Look at organising online event to bring workflow tool developers together with HPC RSEs to explore the space and how these tools can be enabled in MFA world.
    - Maybe look at one of the SORSE events for this
    - IRIS looking at command line access via federated access (via STFC)
  - (AndyT) Raise option of authentication workshop with HPC-SIG
  - (AndyT) Organise presentation on IRIS authentication work to this group

## Topics of interest

### RDF Plans?

  - Plan for future RDF with little/no interruption of service from current service
  - Delivery and development has been delayed by COVID-19 lockdown
  - Hope for more information towards end of Summer 2020

### Organising a GPU course

  - NI-HPC looking to organise GPU courses. How did they do this?
    - NVidia ambassadors have access to lots of training materials
    - Sheffield have lots of experience, see: <https://gpucomputing.shef.ac.uk/>
    - EPCC GPU course: CUDA, OpenMP, OpenACC, see: <https://epcced.github.io/archer-gpu-course/>
  - GPU programming in general
    - CYCL - Used by Intel as their OneAPI
    - OpenCL: <http://uob-hpc.github.io/assets/DoE_PPP_McIntosh-Smith_keynote_Apr_2019.pdfhttps://dl.acm.org/doi/pdf/10.1145/3388333.3388643>
    - OpenMP:  <https://github.com/UoB-HPC/openmp-tutorial>
    - Kokkos: <https://www.exascaleproject.org/event/kokkos-class-series/>

### HPC Training Coordination

  - Would be good to understand what the requirements for the user communities
    - See, for example: <https://www.hpc-certification.org/>
  - Understand what different sites offer and what material is out there already
  - Could different sites/groups work together to coordinate delivery of an HPC training programme?
  - ARCHER2 hoping to feed material into HPC Carpentry
  - UCL working to convert HPC Carpentry for UCL systems and hope to push back useful stuff into the repository (see report below for more detail)
    - Working on MPI material, EPCC also working on this so this work should coordinate between UCL and EPCC

## National HPC RSE Updates

### ARCHER/ARCHER2/Cirrus/DiRAC, EPCC

  - ARCHER2:
    - 1st eCSE call seems to be really popular with lots of applications
    - Lots of work on developing new training. Includes an initial pass on a basic Containers course developed in collaboration with Jeremy Cohen (Imperial College)
  - Cirrus
    - Complete rebuild of system, including move to Slurm and addition of lots of GPU nodes
    - Lots of work to rebuild software packages and update documentation 
    - Looking at how we can configure an EasyBuild toolchain for HPE along the same
      lines as the Cray toolchains
  - DiRAC
    - RSE software development projects continue: SWIFTsimIO functionality, OpenQCD GPU work, AREPO GPU ray tracing and ProMPI GPU porting
    - Tidying up of benchmarking repositories and update of results

### ExCALIBUR benchmarking

  - Working to identify mini-apps and proxy benchmarks to represent algorithms
    of importance for UK research exascale cases
    - Potentially cover seven dwarves of HPC + ML
    - Need to be able to run on experimental hardware with minimal compilers/libraries etc. as well as standard HPC systems
  - Coordination with ExCALIBUR Phase 1 software projects still needs to be picked
    up properly - coordination meeting on 21 July will hopefully provide opportunities
    for this.

### Isambard, GW4

  - Isambard is now SSH key only access
    - Would be useful if the community worked together to define how new access approaches will work
  - You may have heard of a new entry in the Top500 list not much fanfare but Fugaku with it's A64fx chips.  Slightly smaller scale will be joining the expanded Isambard data (date TBC).
  - The upgrade to existing ARM system is delayed, and Cray/HPE are hoping to reuse a team already in Europe for the installation because of the issues with quarantine for arrivals in to the UK.
  - We’ve currently been unloaned the Skylake nodes from the ‘MACs’ (Multi Architecture Comparison system), looking to get some replacement newer generation boxes.
  - The PE 20.06 upgrade on Phase 1 has been cancelled as it is only compatible with RHEL 8. Apparently another site tried to bodge it in on RHEL 7 but it didn't work.
  - In terms of security and authentication we haven't tried anything new, e.g. a way of forcing password changes. hoping to get a wider view of how everyone else is going so we don't have to make too many more all user changes.  It would be good to present a common approach across >=2Tier sites at least?
  - Have a couple of users struggling to get back on, some issues with not using default ssk-keys?

### MMM Hub, UCL

  - Running into some vendor compatibility issues in bringing systems back due to various OS version and driver incompatibilities
  - Key-only login running (as before). Monitoring the system for unsecured SSH keys on the system 
  - We have just started a project with my team and the Research Software Development team to sort out running HPC Carpentry online, and also create some sort of self-directed learning version of it. We are currently comparing with our previous internal in-person training course and seeing if we think anything needs adding. (HPC Carpentry is a lot more succinct than our course, but seems to cover all the necessaries!) We did have a more in-depth section on different types of jobs (serial, OpenMP, MPI and then also array jobs) where we got users to run different versions of one of our pi examples, which we may add back in

### NI-HPC

  - Test users on the system: NAMD and ORCA
  - Hardware audit and inspection to be completed next week
  - Two RSEs starting at beginning of July
  - Open up system for other local users in a couple of weeks

## Upcoming training, events and meetings

  - ARCHER2 Training: [https://www.archer2.ac.uk/training/#upcoming-training](https://www.archer2.ac.uk/training/#upcoming-training)
  - [CarpentryCon@Home](https://carpentries.org/blog/2020/05/2020-carpentrycon-at-home-proposals/)
  - Online Kokkos training, Jul-Aug 2020: <https://www.exascaleproject.org/event/kokkos-class-series/>

## Date of next meeting

1400 UK Time, TBC August 2020
