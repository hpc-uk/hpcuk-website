---
layout: course
title: GPU programming with CUDA and HIP
banner: web_banners_05.jpg 
human_dates: 3rd - 4th May 2023 9:30-17:00, 9:00-16:00 
start_date: 2023-05-03 09:30:00
end_date: 2023-05-04 16:00:00
trainers: Kevin Stratford (EPCC)
course_type: course
registration_status: open
registration_url: https://www.cirrus.ac.uk/training/register/?course=230503-cirrus-gpu
location: Edinburgh (in person)
location_url: https://www.cirrus.ac.uk/training/locations/epcc
prace_course: false
tier2: Cirrus
---

## Location

This course will take place in person in Edinburgh

[Bayes Centre G.03, The University of Edinburgh]({{site.base_url}}/training/locations/epcc "Click for location details, map and directions")

## Overview

This short course will provide an introduction to GPU computing with CUDA aimed at scientific application programmers wishing to develop their own software. The course will give a background on the difference between CPU and GPU architectures as a prelude to introductory exercises in CUDA programming. The course will discuss the execution of kernels, memory management, and shared memory operations. Common performance issues are discussed and their solution addressed. Profiling will be introduced via the current NVIDIA tools.

The course will go on to consider execution of independent streams, and the execution of work composed as a collection of dependent tasks expressed as a graph. Device management and details of device to device data transfer will be covering for situations where more than one GPU device is available. CUDA-aware MPI will be covered.

The course will not discuss programming with compiler directives, but does provide a concrete basis of understanding of the underlying principles of the CUDA model which is useful for programmers ultimately wishing to make use of OpenMP or OpenACC. The course will not consider graphics programming, nor will it
consider machine learning packages.

Note that the course is also appropriate for those wishing to use AMD GPUs via the HIP API, although we will not specifically use HIP.

### Pre-requisite Programming Languages:

Attendees must be able to program in C or C++ (course examples and
exercises will limit themselves to C). A familiarity with threaded programming models would be useful, but no previous knowledge of GPU programming is required. 


Course attendees should bring a laptop, but do not need GPU hardware. Access to a GPU machine (Cirrus) will be provided.


They are also required to abide by the [Cirrus policies](../../../about/policies/tandc.html). 

## Timetable

### DAY  ONE

- 09:30 - 10:00  Logistics and logging in
- 10:00 - 10:30  Introduction and GPU architectures
- 10:30 - 11:00  The CUDA/HIP programming model<br><br>
- 11:00 - 11:30  Break<br><br>
- 11:30 - 12:00  CUDA programming: kernels
- 12:00 - 13:00  A first CUDA exercise: operation on a vector<br><br>
- 13:00 - 14:00  Lunch<br><br>
- 14:00 - 14:30  Programming: memory considerations
- 14:30 - 15:30  Exercise: operation on a matrix<br><br>
- 15:00 - 15:20  Break<br><br>
- 15:20 - 15:45  Unified/managed memory
- 15:45 - 16:00  Exercise: managed memory
- 16:00 - 16:20  Threaded programming and synchronisation
- 16:20 - 17:00  Exercise: Reduction for vector product
- 17:00          Close


### DAY  TWO


- 09:00 - 09:10  Detour: using profiling
- 09:10 - 10:00  Exercise: nsight and nsight systems
- 10:00 - 10:40  Device Management. The idea of streams; its extension to CUDA Graph API
- 10:40 - 11:00  Exercise: graph API<br><br>
- 11:00 - 11:30  Break<br><br>
- 11:30 - 12:00  More than one GPU: GPU to GPU transfers GPU aware MPI
- 12:00 - 13:00  Exercises (cont.)<br><br>
- 13:00 - 14:00  Lunch<br><br>
- 14:00 - 14:10  Put it all together: Conjugate gradient (CG) algorithm
- 14:10 - 15:00  CG exercise<br><br>
- 15:00 - 15:20  Break<br><br>
- 15:20 - 15:50  CG exercise (cont.)
- 15:50 - 16:00  Some miscellaneous observations
- 16:00          Close

<section id="service">





</section>


