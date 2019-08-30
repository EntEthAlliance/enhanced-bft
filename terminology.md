
# Categories of Terms

| Label | Category | 
--------|------------
| CP    | Core Property |
| F     | Faults  |
| N     | Network | 

# Terminology

In order alphabetically by `Label` then by `Term`, or just `Term` if there is no `Label`.  

|Label | Term                                | Definition      |
|------| ----------------------------------  | --------------- |
| CP | Liveness             | Every correct propsed value will eventually be accepted by correct nodes. aka something good happens. | 
| CP| Persistence         | ??
| CP | Safety              | If a value is committed by a correct node, then that value will eventually be commited by all correct nodes. Two correct nodes will never commit to different values. aka nothing bad happens. 
|| Cryptographic Hash Function         | A collision resistant hash function that cannot feasibly be reversed by a computationally bound adversary.
|| Global Stabalization Time (GST)     | "A time unknown to the processors, such that the message system respects the upper bound from time GST onward." (DLS Consensus in the Presence of Partial Synchrony) 
|| Linearizability                     | 
|F | Fault Tolerance                     | A system / protocol can handle faults in system, where nodes die and never deliver messages. 
|F | Byzantine Fault Tolerance           | Can handle faulty nodes including malicious (Byzantine nodes) that may collude, send arbibrary data, delay correct nodes, or not send data at all.
|F | Optimally Byzantine Fault Tolerance | Can handle `n - 1/ 3` byzantine nodes, the minimum number of replicas in the network must be `3f + 1` where  up to `f` may be byzantine nodes. This is a proven upper bound.  
|N | Asynchronous Network                | No known bounds on message delivery.
|N | Synchronous Network                 | Known bounds on message delivery, and processing time.
|N | Partially Synchronous Network       | Known bounds on message delivery with periods of instablity where the network turns asynchrous. The normal state of the network assumes upper bounds on message delivery, however when the network is unstable, this upper bound is not respected. (DLS - "Consensus in the presence of faults")
|N | Weak Synchrony              | (same as partially synchronous) "The network can be asynchronous (i.e., entirely controlled by the adversary) for a long but bounded period." (Algorand)
|| Quorum Certificate (QC)             | A (cryptographically signed) set of votes from a quorum of nodes in the system.
|| Responsiveness                      | "A non-faulty proposer can drive the protocol to consensus in time depending only on the actual message delays, independent on any known upper bounds on message delays." (YMRGA Hotstuff: BFT Consensus in the Lens of Blokchain)
|| Optimal Responsivess                | Responsiveness ony after GST is reached.
|| Robustness                          | Preserves safety and liveness. 
|| View Change                         | The phase that occurs after a primary fails. Protocol for changing the proposer. 
