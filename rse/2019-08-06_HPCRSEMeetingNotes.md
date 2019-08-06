---
layout: page
title: HPC RSE Meeting Notes: 6 Aug 2019
summary:
---

# Attending organisations

   - ARCHER (Tier1), Cirrus (Tier2): EPCC, The University of Edinburgh
   - Cumulus (Tier2): University of Cambridge
   - Isambard (Tier2): GW4, Univeristy of Bath
   - Aberystwyth University, Supercomputing Wales
   - University of Southampton

# Actions

   - (EPCC) Check with EPSRC about status of Autumn RAP Open Access to Tier-2 call

# Meeting format

   - National service RSE groups will post an update to the HPC-UK website on highlights from the past month
   - Invite for all to join will point to updates as potential starting point for discussions and request other items for discussion
   - All will be invited to add upcoming training and events that are of interest and there will be a standing agenda item covering training and events

# RSE Updates

## Cumulus

   - Been investigating how well MPI HPC applications work over high performance ethernet compared to infiniband up to typical job size for Cumulus (maximum of 32 nodes)
      + Presenting the work at MPICH User Group meeting in September
      + Short story is that there is no significant difference in performance when using ethernet rather than IB - even for all-to-all heavy codes such as CASTEP
      + Will write up and circulate
   - Question about whether the Tier2 RAP Open Access call will run in Autumn or not
   - If Tier-2 will be used for gap between ARCHER and ARCHER2, we need to start work on porting researchers across soon
      + What is the plan for RSE support for ARCHER projects on Tier-2? Will it be supported by ARCHER CSE, Tier-2 RSE or both?

## Isambard

   - First set of RAP projects on the system now - do not seem to have been any major issues porting their work and getting up and running
   - Bath have been working on getting VASP, QE and NAMD users onto system
      + Plans to get OpenFOAM users up and running soon
   - Workshop in Cardiff in July run by GW4 RSE and Arm
      + Looked at performance of VASP with ArmPL compared to Cray LibSci:
      + std and ncl versions: 10-30% faster with ArmPL compared to LibSci
      + gam version: 20% slower with ArmPL compared to LibSci
      + Investigations ongoing
   - Question about portability of CASTEP licence
      + Licence is for source so you can run on any system with an Academic licence

   - Also been looking at running rsearch software in the commercial cloud
      + Attended the RSE Summit organised by MS in Brussels
      + One of the outcomes was the Research Software Reactor: https://github.com/research-software-reactor
      + Provide one-click blueprints to allow researchers to run in the commercial cloud (Azure at the moment)

## ARCHER, Cirrus

   - Been looking at MPI performance across different platforms and different MPI libraries using IMB 
   - Started out as we had seen poor CASTEP scaling on Arm-based systems which was tracked down to Alltoallv scaling issues
   - Full set of results and analysis at: https://github.com/hpc-uk/archer-benchmarks/tree/master/synth/IMB

   - Most detailed analysis so far on Alltoallv performance: https://github.com/hpc-uk/archer-benchmarks/blob/master/synth/IMB/analysis/IMB_Alltoallv_compare.ipynb
      + Arm-based systems show 10-20% peformance of Cray Aries dragonfly, irrespective of interconnect technology and MPI library for fully-populated nodes
      + Arm: Halving the number of MPI ranks per node doubles the MPI performance on Cray Aries for medium to large messages
      + Arm: Halving the number of MPI ranks per node increases the performnace by 5-6x on IB for medium to large messages
      + Have not yet investigated the effect of tuning parameters
      + Topology seems to have a large effect on OPA performance even though all runs are within a single non-blocking switch: compare Cumulus to Tesseract in the results.

# Other topics

## Cloud bursting

   - Has cloud bursting from on-prem HPC to commercial cloud been tried by anyone and, if so, how well has it worked?

   - University of Liverpool HPC have a solution with AWS that is supposed to do this using Condor HT
      + Latest reports are that this approach is working fine

   - Storage is a challenge when running HPC workloads in the cloud.

   - Software licences are usually OK.

   - Portability approach differs between HPC and cloud
      + HPC portability usually achieved by recompiling source code against hardware specific libraries and MPI
      + Cloud portability usually achieved with binary in VM/containers that can run on "any" hardware. 

##  Do you need IB for shared NFS file systems?

   - If this is being passed over TCP/IP (e.g. IP over IB) then unlikely to see performance improvements for IB if you are using high-bandwidth ethernet (e.g. 25-50 Gbps)
      + Some NFS vendors may provide direct NFS via ibverbs that could improve performance

# Upcoming training, events and meetings

   - ATI Data Study Event, Bristol, Aug 2019
      + Data provided
      + Azure resource to analyse the data
   - OpenMP on GPU Virtual Tutorial by Mark Bull, EPCC: http://www.archer.ac.uk/training/virtual/index.php
   - RSE for HPC Meeting, Birmingham, PM 16 Sep 2019
      + Associated with RSEConUK19, Birmingham
      + James Grant (Bath) and Jo Beech-Brandt (EPCC) organising
      + [Registration link](https://docs.google.com/forms/d/e/1FAIpQLSdId3jE3Z2v9aq_ylHrsh9ybu-pU0ojXj7ae5xrks-vZLAHiw/viewform?usp=sf_link)
   - RSEConUK 2019, Birmingham, 17-19 Sep 2019
      + Tickets selling out fast!

   - Upcoming ARCHER Training Opportunities. Full details and registration at http://www.archer.ac.uk/training/index.php
      + OpenMP on GPUs, Virtual Tutorial, Wednesday 28th August 2019 15:00
      + Enabling distributed kinetic Monte Carlo simulations for catalysis and materials science, Webinar, Wednesday 25th September 2019 15:00
      + Programming the ARM64 processor, University of Cambridge, 30 Sep - 1 Oct 2019
      + Hands-on Introduction to HPC for Life Scientists, University of Birmingham, 30 Oct - 1 Nov 2019
      + Shared-memory Programming with OpenMP - Online course, four Wednesday afternoons, 13, 20, 27 November and 4 December 2019

# Date of next meeting

1400 BST, Tue 3 Sep 2019
