---
layout: page
title: UK HPC RSE Network
summary: Sharing expetise on supporting HPC
---

# Attending organisations

   - ARCHER (Tier1), Cirrus (Tier2): EPCC, The University of Edinburgh
   - Cumulus (Tier2): University of Cambridge
   - HPC Mid+ (Tier2): Loughborough University
   - MMM Hub (Tier2): UCL
   - Isambard (Tier2): GW4, Univeristy of Bristol
   - Cardiff University, Supercomputing Wales
   - University of Bristol
   - University of Nottingham

# RSE Updates

## ARCHER, Cirrus

   - Been looking at different ways of delivering online training to allow for scale
     out (both externally and for multiple locations within a single institution).
   - Models tested:
      + Lecturer in classroom, attendees joining in person or remotely: doing the exercises remotely during sessions did not work
      + Lecturer in classroom, attendees joining in person or remotely: doing the exercises between lecture sessions worked with 
        "catchup" lecture on the practical at the start of the next online session
      + Lectures recorded, exercises/assessments distributed online, attendees join online tutorials to discuss exercises/assignments:
        technology (Blackboard Collaborate) worked well but tutorials had low attendence
      + Articles on topics followed by online discussion (MOOC) using FutureLearn technology: Worked very well with good engagement
        with discussion
   - In all cases, except the MOOC on FutureLearn, building peer interactions and a sense of commnity during the courses has 
     proved very difficult.
      + The specific design of the MOOC and the FutureLearn platform with the course built around discussion made this part 
        of the courses work well
   - Also investigating how we could deliver Carpentries-style learning online/remotely

   - Done a lot of work on benchmarking and performance comparison between different UK HPC systems.
      + Used an Open Source methodology with all raw data, analysis notebooks, build instructions etc. publicly available
      + See: [https://github.com/hpc-uk/archer-benchmarks](https://github.com/hpc-uk/archer-benchmarks)

## HPC Mid+

   - RSE's lookng after assessing and staffing RSE projects proposed by HPC Mid+ partners
   - Developed extremely popular Scientific Python course that has been delivered at L'boro multiple times and is extremely popular
     + Looking at how to scale out across other HPC Mid+ institutions
     + See: [https://github.com/luitfc/Introduction-to-Scientific-Python](https://github.com/luitfc/Introduction-to-Scientific-Python)
   - Other training in development (initially aimed at CFD code developers):
     + Application profiling using Intel tools
     + Vectorisation
   - Working on optimising particular packages and producing guidance. Initially: OpenFOAM, LAMMPS
   - Coordinating an OpenFOAM user community at L'boro
    
## Isambard

   - Isambard is the Arm-based Tier2 system (possibly the first production Arm-based HPC system in the world)
   - Done a lot of work on benchmarking and performance characterisation in support of the new architecture
      + Take top usage codes from ARCHER and look at performance on Arm
      + Aim to be as open and reproducible as possible, see: [https://github.com/UoB-HPC/benchmarks](https://github.com/UoB-HPC/benchmarks)
   - RSEs can get access to Isambard to test applications on Arm
   - Run regular hackdays to get codes ported and performing on Arm

## MMM Hub

   - Annual MMM Hub conference; 3-4 Sep 2019
   - Seen issues with having Intel 2018 MKL and MPI as default. Currently planning move to Intel 2019 stack
      + EPCC reported that DiRAC have seen lots of issues with Intel MPI 2019; hanging in Allreduce and 
        issues with MPI-IO. All work in IMPI 2018
   - Also thinking of moving to GCC as the default environment on the system (rather than Intel)
   - Have a large collection of scripts used to build centrally-installed software on the service that may 
     be useful for other people: [https://github.com/UCL-RITS/rcps-buildscripts](https://github.com/UoB-HPC/benchmarks)

## Cumulus

   - Cumulus/CSD3 is a diverse set of hardware all connected to the same, high-performance storage
      + May be particularly helpful for researchers with workflows that require different hardware at different stages
   - Creating tools that sit on top of the Spack tool to help it manage package installs better
      + EPCC noted that Spack are working on functionality called Spack Environments that may help
      + Bristol noted that EasyBuild as an alternatve was neither Easy, nor did it Build. They have had
        a roughly 50% success rate with Spack
      + EPCC noted that there is an active EasyBuild community in the UK HPC-SIG
   - Recently deployed a very high performance, solid state storage system that is number 1 in the IO-500 list
      + Keen to hear from researchers/RSEs that may find this useful
   - Looking at builing a framework for continuous testing/monitoring of the system and software environment
      + Based on Reframe from CSCS
      + EPCC are also looking at Reframe for this purpose - should coordinate on this
      + Another option is a tool called Buildtest

# Other topics

## What experience have people had with Singularity containers?

   - Cumulus/CSD3: SLURM+MPI+Singularity sort of works - had some success using MPICH. Composing workflows that use applications in 
     two (or more) separate containers has proven difficult.
   - Cardiff: used to solve issues where users had complex depenencies. Not much success with OpenMPI
   - MMM Hub: used to enable custom serial environments
   - EPCC: used to enable custom serial environments. Not had much success in creating an MPI configuration
     that could be used by a normal user.
   - Looks like Singularity should work on Arm

## HPC in the Cloud (Bristol report)

   - Discovered a bug in Intel MKL DNN library when running in a cloud VM - escalated to Intel
   - Had success with Cluster in the Cloud and are presenting at RSEConUK19 on this:
      + [https://rseconuk2019.sched.com/event/QSQk/3b2-hpc-and-novel-clusters-zero-to-cluster-in-20-minutes-there-and-back-again](https://github.com/UoB-HPC/benchmarks)
      + [https://cluster-in-the-cloud.readthedocs.io/en/latest/](https://github.com/UoB-HPC/benchmarks)
      + Add Singularity to Cluster in the Cloud: [https://github.com/christopheredsall/citc-singularity](https://github.com/UoB-HPC/benchmarks)
      + Test for MPI with Singularity: [https://github.com/christopheredsall/singularity-hello-world](https://github.com/UoB-HPC/benchmarks)
   - EPCC noted the challenges of getting good IO performance on clusters in the cloud

# Upcoming events and meetings

   - ATI Data Study Event, Bristol, Aug 2019
      + Data provided
      + Azure resource to analyse the data
   - RSE for HPC Meeting, Birmingham, PM 16 Sep 2019
      + Associated with RSEConUK19, Birmingham
      + James Grant (Bath) and Jo Beech-Brandt (EPCC) organising
      + [Registration link](https://docs.google.com/forms/d/e/1FAIpQLSdId3jE3Z2v9aq_ylHrsh9ybu-pU0ojXj7ae5xrks-vZLAHiw/viewform?usp=sf_link)
   - RSEConUK 2019, Birmingham, 17-19 Sep 2019
      + Tickets selling out fast!

# Date of next meeting

1400 BST, Tue 6 Aug 2019