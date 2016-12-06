========================================================
Functional & Pipeline Simulator for simpleRISC processor
========================================================

README

Table of contents
1. Directory Structure
2. How to build
3. How to execute

Directory Structure:
--------------------
CSL211-Project
  |
  |- bin
      |
      |- sim
  |- include
      |
      |- Core.h
      |- Memory.h
      |- PipelineRegister.h
      |- Register.h
  |- src
      |- main.cpp
      |- Core.cpp
      |- Memory.cpp
      |- PipelineRegister.cpp
  |- test
      |- simple_add.mem
      |- fib.mem
      |- array_add.mem
      |- assign4.mem

How to build
------------
For building:
	$make

For cleaning the project:
	$make clean

How to execute
--------------

$./bin/sim (Input_MEM_file_path) [0 | 1] [0 | 1 | 2]

III argument
* Optional
* 0 for Single Cycle Based
* 1 for Pipeline Based
* Default 0

IV argument
* Optional
* Specify level of prinitng
* 0 for recording .print statements
* 1 for recording accesses to Memory & updates to Register File
* 2 for recording all signals at every cycle
* Default 0


The code generates a DATA_OUT.mem i.e. the complete memory at the termination of program 
and a STATE_OUT.mem i.e. complete state of processor at the termination of program.

The output contains instruction by instruction work done in each cycle in all stages namely -

1. FETCH
2. DEOCDE
3. EXECUTE
4. MEMORY ACCESS
5. WRITEBACK

Developed by
Naman Goyal (email: 2015csb1021@iitrpr.ac.in)
Supervised by
Dr. Neeraj Goel (email: neeraj@iitrpr.ac.in)
