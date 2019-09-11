
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
|F | Byzantine Fault Tolerance           | Can handle faulty nodes including malicious (Byzantine nodes) that may collude, send arbitrary data, delay correct nodes, or not send data at all.
|F | Consensus Protocol with Optimal Byzantine Fault Tolerance in Partially Synchronous and Asynchronous Networks | Consensus protocol that can withstand up to `floor((n - 1)/ 3)` Byzantine nodes when operating in either a partially synchronous or asynchronous network where `n` is the total number of the nodes participating in the consensus protocol. As a consequence of this, the number `n` of nodes participating in the consensus must be `n >= 3f + 1` where `f` corresponds to the maximum number of Byzantine nodes. This is a proven upper bound on the number of Byzantine nodes.  
|N | Asynchronous Network                | No known bounds on message delivery.
|N | Synchronous Network                 | Known bounds on message delivery, and processing time.
|N | Partially Synchronous Network       | There exits a finite, but unknown, upper bound on the message latency [1].
|N | Eventually Synchronous Network       | From [1]:<br><ul><li>There exists a finite, but unknown, point in time called `GST` (Global Stabilization Time).</li> <li>There does not exist any upper bound on the latency of messages sent before `GST`.</li> <li>Messages sent before `GST` may never reach destination.</li><li>There exists a finite upper bound $\Delta$ on the latency of messages sent at a time greater than, or equal to, `GST`.</li><li>The value of $\Delta$ unknown.</li></ul>
|N | Weak Synchrony              | (same as partially synchronous) "The network can be asynchronous (i.e., entirely controlled by the adversary) for a long but bounded period." (Algorand)
|| Quorum Certificate (QC)             | A (cryptographically signed) set of votes from a quorum of nodes in the system.
|| Responsiveness                      | "A non-faulty proposer can drive the protocol to consensus in time depending only on the actual message delays, independent on any known upper bounds on message delays." (YMRGA Hotstuff: BFT Consensus in the Lens of Blokchain)
|| Optimal Responsivess                | Responsiveness ony after GST is reached.
|| Robustness                          | Preserves safety and liveness. 
|| View Change                         | The phase that occurs after a primary fails. Protocol for changing the proposer. 

[1] C. Dwork, N. Lynch, L. Stockmeyer, *Consensus in the presence of partial synchrony*, J. ACM 35 (2) (1988) 288323. doi:10.1145/42282.42283. URL http://doi.acm.org/10.1145/42282.42283
