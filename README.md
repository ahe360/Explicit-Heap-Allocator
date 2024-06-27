Copyright (c) 2002, R. Bryant and D. O'Hallaron, All rights reserved. 
May not be used, modified, or copied without permission

# Dynamic Storage Alocator

Implementation of an explicit heap allocator with an explicit free-list with LIFO replacement policy, written in C. Includes trace files for debugging, and driver program for testing.

# Main Files:

mm.{c,h}
	Solution malloc/free package. mm.c is the primary file that implements memory allocation logic

mdriver.c
	Testing file for mm.c

Makefile
	Builds the driver

# Support files for the driver

config.h	Configures the malloc lab driver
fsecs.{c,h}	Wrapper function for the different timer packages
clock.{c,h}	Routines for accessing the Pentium and Alpha cycle counters
fcyc.{c,h}	Timer functions based on cycle counters
ftimer.{c,h}	Timer functions based on interval timers and gettimeofday()
memlib.{c,h}	Models the heap and sbrk function

# Testing
To build the driver, type "make" to the shell.

To run the driver on all traces:

    unix> ./mdriver

To run the driver on a tiny test trace:

	unix> ./mdriver -V -f short1-bal.rep

The -V option prints out helpful tracing and summary information.

To get a list of the driver flags:

	unix> ./mdriver -h

