The goal of this work is to agree on an interoperable consensus protocol that meets the following requirements:

* MUST guarantee Optimal Byzantine Fault Tolerance for Partially Synchronous and Asynchronous Networks
* MUST have a formal proof of correctness that we can show to regulators;
* MUST guarantee timely finality;
* MUST guarantee all of the requirements listed here when operating in eventually synchronous network
* SHOULD have a specification sufficient to enable implemetation without having to refer to someone else's code;
* The consensus algorithm MUST support the following safety and liveness properties
  - Agreement — Two different processes MUST decide the same block (agree on the same block).
  - Validity — If a process decides on a block, then that block must have been proposed by some process. Secondly the proposal itself must be a valid block. 
  - Integrity — A process MUST only decide for a block at most once (in a round)
  - Termination — Each honest process MUST eventualy decide (ensuring progress)
