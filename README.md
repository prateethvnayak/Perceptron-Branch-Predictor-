# Perceptron-Branch-Predictor-
Branch Prediction in microarchitecture level using single layer perceptron in SimpleScalar

The branch predictors like 2-level and bimodal have relatively lesser accuracy compared to a nerual based branch predictor. Hence we use th SimpleScalar tool to implement a perceptron algorithm to increase the accuracy of the branch predictions of the programs. 

The file bpred.c is changed accordingly to accomodate the perceptron predictor also. The arguments while running the SimpleScalar simulation are used to switch between the different types of predictors to see the accuracy. 

Simple_Scalar 
SimpleScalar is a suite of processor simulators and tools used for simulating real programs running on a modern processor and systems. It is used to build modeling applications for program performance analysis, detailed micro-architectural modeling, and hardware-software co-verification.
The tool set includes sample simulators ranging from a fast functional simulator to a detailed, dynamically scheduled processor model that supports non-blocking caches, speculative execution, and state-of-the-art branch prediction. Basically, SimpleScalar is a C program which models a processor and it accepts the programs (that could run on this hypothetical processor) as arguments.
SimpleScalar simulators can emulate the Alpha, PISA, ARM, and x86 instruction sets, and these are very similar to the MIPS architecture that will be discussed in EE5364/CSCI5204.
SimpleScalar was developed at the University of Wisconsin in Madison and is one of the most widely used architectural simulators in academia.

Get the simulator and a sample benchmark
a. Download the simplesim-3v0e.tar file from http://www.simplescalar.com/ and untar it. This will create the folder simplesim-3.0
b. Download the sample benchmark (anagram) from same website.
c. It is strongly recommended that you read the README before continuing to the next step.

d. Change to the directory simplesim-3.0 and run the following commands
  i. make clean
  ii. make config-alpha
  iii. make
  If you see the message “my work here is done….”, then you have successfully installed SimpleScalar on your machine.
e. You now have the following simulators:
     i. Functional: sim-safe, sim-fast
     ii. Cache: sim-cache
     iii. Profiling: sim-profile
     iv. Out of order processor: sim-outorder
f. You may run “./sim-outorder” in the simplesim-3.0 directory to get the manpages for SimpleScalar. It gives a list of all possible arguments that SimpleScalar can accept that are used to model the processor architecture.

Running the simulation
1. Go to the directory containing the anagram benchmark and run:
  ./<path_to_sim-outorder>/sim-outorder anagram words < anagram.in
  This will take about a minute to run and will give the output of anagram, as it ran on SimpleScalar. It will also give the      output of SimpleScalar on the terminal, which will the simulation statistics.
  If you can see the simulation statistics and the output of anagram (similar to anagram.out), then your simulation has         completed without any error.
2. As an example, if you wish to change the latency of your caches, then you may run:
    ./<path_to_sim-outorder>/sim-outorder -cache:dl1lat 2 -cache:dl2lat 12 anagram words < anagram.in
    

  If you can see the simulation statistics and the output of anagram (similar to anagram.out), then your simulation has         completed without any error.
  
  Then changing the SimpleScalar C/C++ files with the one in repo helps integrate the nerual predictor. The statistics can be seen in the output by selecting the predictor type as 'nerual' on running. 
  
