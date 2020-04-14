---
layout: page
title: HPC RSE Meeting Notes: 24 March 2020
summary:
---

# HPC RSE Meeting Notes: 24 March 2020

## Attending organisations

   - EPCC: ARCHER, ARCHER2, Cirrus, DiRAC
   - QUB: NI-HPC
   - GW4: Isambard Bath, Bristol
   - JADE: Sheffield
   - Aberystwyth University
   - Imperial College
   - University of York
   - University of Birmingham
   - UCL 

## Actions

   - (AndyT) Propose SocRSE online event on online training this year to SocRSE trustees

## National HPC RSE Updates

### ARCHER, ARCHER2, Cirrus, DiRAC, EPCC

   - DiRAC benchmarks
     + Application benchmarks from the community - QCD, astrophysics/cosmology
     + Baseline across current DiRAC systems
     + Release in open source benchmarking model (as for ARCHER benchmarks)
   - Oracle bare metal cloud benchmarking
     + Skylake nodes interconnected by 100 Gbps RoCE
     + Benchmarked DiRAC benchmark applications up to 16 nodes
     + Single node performance same as native
     + Multi-node performance similar to single-rail IB cluster
  
  - Cirrus2 funded - GPU-based IB system
    - Hardware on site and being installing as we speak

  - ARCHER extended to June 2020
    + Support continuing (minus training and eCSE)
    + Investigating feasibility of Spack/EasyBuild on Cray systems to prepare for ARCHER2
    + Have early access to Fujitsu A64fx processors to run benchmarks

  - ARCHER2
    + SP and CSE contracts awarded to EPCC
    + ARCHER2 hardware delayed
    + SP and CSE still due to start on original timescale
    + Working to develop initial training building on HPC Carpentry existing lessons - plan to 
      contribute these back as open source as part of HPC Carpentry

### Isambard, GW4 

  - Isambard up and running
  - Isambard2 funded: Cray/HPE system, second cabinet of Marvell TX2 XC50, cabinet of 72 Fujitsu A64FX, multi-architecture testbed extension

### NI-HPC

  - 8,000 cores AMD + NVidia GPUs + EDR Infiniband
  - All arrived and racked
  - Dell running tests at the moments
  - Handover to Alces for testing after that
  - On track to start service as planned
  - Interviewing for RSEs at the moment, may need to re-advertise

### JADE/JADE-2

  - 63 nodes of DGX maxQ nodes - more power efficient 
  - 70 TB of solid state storage
  - Plan for hardware by end of March and service by end of June
  - Plan to use for RAP

## Other topics

### Report from HPC Champions

  - Intro to new Tier2 providers 
    - Interest in harmonising access across sites: Instant Access/Pump Priming/Seedcorn, etc.
    - Instantiating Driving Test across all sites. EPCC to share questions and approach
    - Potential lightweight application process that is easier than RAP (Consortia already do this on Tier1, ARCHER). Bridge gap between Instant Access and RAP
    - Look at making the TA a more collaborative process between RSE team and applicant (for some sites this is already how it works)
  - Sharing training resources (e.g. on HPC-UK)
  - Looked at knowledge base and what it would cover, what areas are interesting

### Online and remote

 - Online training:
   - Lots of people trying out different approaches
   - EPCC tried various things and plan to run webinar with experiences in next week or so
   - GW4 (Bristol) ramping up online training before Easter to try different things
   - Interesting blog post from Greg Wilson
   - Chris CA: Carpentry with small pre-recorded lectures
   - AndyT has some experience of pre-recorded lectures for a traditional Uni course 
   - Online Carpentries Instructor Training 
 - Online workshops
   - SSI interview process worked well for online workshops, good idea for online workshops
 - Useful online training that you can base courses on
   - CodeRefinery: https://coderefinery.org/
   - Carpentries: https://carpentries.org/
 - Online HPC Support
   - Replacements for drop-in support sessions: Zoom seems to support remote control but not tried yet (Imperial)
   - Sheffield looking at using remote control in Google hangouts to provide online support
   - ARCHER users are all remote from EPCC so used traditional service desk with support (i.e. via e-mail)

#### Useful links from meeting chat

   -  https://milliams.com/posts/2020/online-workshop-reflections/ 
    - I've definitely made use of the recorded Archer and POP webinars 
   - https://education.rstudio.com/blog/2020/03/teaching-online-on-short-notice/  Slides http://rstd.io/teach-online-2020
   - Q&A https://education.rstudio.com/blog/2020/03/online-teaching-qa/ 
   -  Jason Bell, Senior Research Technologies Officer at CQUniversity, recently gave a presentation on “Virtual Software Carpentry Workshops - key learnings to make it a success” in a webinar organised by Australian Research Data Commons. https://carpentries.us14.list-manage.com/track/click?u=46d7513c798c6bd41e5f58f4a&id=7b8366d2f7&e=4ed70a0d66 join in on discussions about remote teaching of Carpentries workshops: https://carpentries.us14.list-manage.com/track/click?u=46d7513c798c6bd41e5f58f4a&id=d5114f572e&e=4ed70a0d66 
   -  https://arc-lessons.github.io/courses/00_schedule.html 
   -  https://coderefinery.org/

### Other

 - Singularity: passing environment variables, answered in RSE Slack
   - It turns out that singularity just passes the entire host environment through by default.
   - If you need isolation you can do `--cleanenv` (environment) or `--containall` (filesystems).
   - `SINGULARITY_ENV` prefix too
   - See: https://sylabs.io/guides/3.5/user-guide/environment_and_metadata.html
 - RDF status
   - RDF no longer available for NERC projects
   - RDF continues for EPSRC projects - data to be migrated to new RDF service sometime in 2020 (may be delayed due to COVID-19 situation).

## Upcoming training, events and meetings

  - RSECon 2020 cancelled

## Date of next meeting

1400 UK Time, TBC Apr 2020 (avoid Easter week)
