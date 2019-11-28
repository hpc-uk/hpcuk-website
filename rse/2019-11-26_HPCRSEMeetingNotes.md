---
layout: page
title: HPC RSE Meeting Notes: 26 November 2019
summary:
---

# Attending organisations

   - EPCC, The University of Edinburgh (ARCHER, Cirrus)
   - University of Bath (GW4 Isambard)
   - University of Birmingham, University of Aston (HPC-Mid+)
   - University of Cambridge
   - University of Manchester
   - University of Nottingham
   - Trinity College Dublin
 
# Actions

   - (Andy Turner, EPCC) Put out vote for updated time for the meeting
     - Done. 2pm Tuesdays confirmed as least-worst time

# National HPC RSE Updates

## ARCHER, Cirrus, EPCC

   - MPI benchmarks across a wide variety of systems and MPI libraries now available at: [https://github.com/hpc-uk/archer-benchmarks/tree/master/synth/IMB](https://github.com/hpc-uk/archer-benchmarks/tree/master/synth/IMB)
   - Most complete performance analysis so far is for Alltoallv (as it is important for CASTEP and we were looking at the performance of this specifically), see: [https://github.com/hpc-uk/archer-benchmarks/blob/master/synth/IMB/analysis/IMB_Alltoallv_compare.ipynb](https://github.com/hpc-uk/archer-benchmarks/blob/master/synth/IMB/analysis/IMB_Alltoallv_compare.ipynb)
     + Issues with collectives on Arm systems that are not understood yet

   - Managed to get multi-node MPI Singularity container jobs running on Cirrus. Performance is close to native (non-container) runs
     + Plan to publish technical report or blog article on this

   - Moving ReFrame system regression testing framework into production on Cirrus
     + ReFrame: [https://reframe-hpc.readthedocs.io/en/stable/](https://reframe-hpc.readthedocs.io/en/stable/)
     + Cirrus configuration and initial tests: [https://github.com/EPCCed/epcc-reframe](https://github.com/EPCCed/epcc-reframe)

## Isambard, GW4

   - Continues to attract new users interested in Arm.
   - 70 attendees at OpenMP workshop on GPU @ SC19 using Isambard
   - Should be able to provide more specific updates once the annual report is submitted at the end of the month

## HPC Mid+

   - Drop in usage recently - chasing users to try get people to use it up
     + Comment that fluctuations in usage are often seen - tempting to try and post-rationalise to events or other things going on but very difficult to actually link drops to real sociological causes.
   - Struggling to get licensed software configured and running correctly
     + Many sites noted that they also have problems with this 

# Other topics

## Reporting service metrics 

   - How do different services report service time?
     - Depends on ticketing system
     - Question maybe more suited to the HPC-SIG

## Shared HPC RSE knowledge base

   - Blog article on shared UK HPC knowledge base published at: [http://www.epcc.ed.ac.uk/blog/2019/11/uk-public-hpc-knowledge-base](http://www.epcc.ed.ac.uk/blog/2019/11/uk-public-hpc-knowledge-base)
   - Will propose discussion of this as a topic for the next HPC-SIG meeting and plan to do something at next HPC Champions workshop (if not before)
   - May also put in a proposal for the next RSE conference on this

## HPC Champions

   - Started to think about HPC Champions workshops for next year

# Upcoming training, events and meetings

   - Upcoming ARCHER Training Opportunities. Full details and registration at [http://www.archer.ac.uk/training/index.php](http://www.archer.ac.uk/training/index.php)
      + Shared-memory Programming with OpenMP - Online course, four Wednesday afternoons, 13, 20, 27 November and 4 December 2019
      + Enabling multi-node MPI parallelisation of the LISFLOOD flood inundation model, Online webinar, 4 December 2019 15:00
      + HPC Carpentry, EPCC, Edinburgh, 9-10 December 2019
      + Hands-on Introduction to HPC, EPCC, Edinburgh, 7-8 January 2020
      + GPU Programming with CUDA, EPCC, Edinburgh, 9-10 January 2020
      + Advanced MPI, Imperial College London, 27-28 January 2020

# Date of next meeting

1400 UK Time, TBC Jan 2019
