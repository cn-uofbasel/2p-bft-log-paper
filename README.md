# *2P-BFT-Log*: 2-Phase Single-Author Append-Only Log for Adversarial Environments, Erick Lavoie, [Arxiv Pre-Print Paper](https://arxiv.org/abs/2307.08381)

Keywords: state-based CRDT, append-only log, security

<details>
<summary>Abstract</summary>
      
> Replicated append-only logs sequentially order messages from the same author such that their ordering can be eventually recovered even with out-of-order and unreliable dissemination of individual messages. They are widely used for implementing replicated services in both clouds and peer-to-peer environments because they provide simple and efficient incremental reconciliation. However, existing designs of replicated append-only logs assume replicas faithfully maintain the sequential properties of logs and do not provide eventual consistency when malicious participants fork their logs by disseminating different messages to different replicas for the same index, which may result in partitioning of replicas according to which branch was first replicated.
> 
> In this paper, we present 2P-BFT-Log, a two-phase replicated append-only log that provides eventual consistency in the presence of forks from malicious participants such that all correct replicas will eventually agree either on the most recent message of a valid log (first phase) or on the earliest point at which a fork occurred as well as on an irrefutable proof that it happened (second phase). We provide definitions, algorithms, and proofs of the key properties of the design, and explain one way to implement the design onto Git, an eventually consistent replicated database originally designed for distributed version control.
>
> Our design enables correct replicas to faithfully implement the happens-before relationship first introduced by Lamport that underpins most existing distributed algorithms, with eventual detection of forks from malicious participants to exclude the latter from further progress. This opens the door to adaptations of existing distributed algorithms to a cheaper detect and repair paradigm, rather than the more common and expensive systematic prevention of incorrect behaviour.
</details>

<details>
<summary>BibTex Citation</summary>

````
@misc{lavoie20232pbftlog,
      title={2P-BFT-Log: 2-Phase Single-Author Append-Only Log for Adversarial Environments}, 
      author={Erick Lavoie},
      year={2023},
      eprint={2307.08381},
      archivePrefix={arXiv},
      primaryClass={cs.DC}
}
````
</details>
