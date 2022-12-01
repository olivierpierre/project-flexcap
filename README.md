* * *
**News**
- 11/2022 We have ported a minimal version of Unikraft on the Morello machine, check out the code [here](https://github.com/jkressel/uk-plat-morello)

* * *

## Project Description

In the FlexCap project, we propose to explore the benefits brought by hardware capabilities to operating systems' safety, performance and memory consumption. To that aim we propose to port two operating systems, [FlexOS](https://project-flexos.github.io/) and [Unikraft](https://unikraft.org/), to the ARM [Morello](https://www.arm.com/architecture/cpu/morello) platform, and investigate in that context the two main features provided by capabilities: efficient/scalable compartmentalization, and safe version of legacy programming languages through pure/hybrid capabilities.

FlexOS is a safety-oriented library operating system in which the safety/isolation strategy can be easily tailored at build time towards a specific application use case. Many safety options can be configured, including in particular the granularity of kernel/user components isolation and the hardware mechanism enforcing that isolation. We expect that leveraging the efficient compartmentalization features of hardware capabilities in FlexOS will bring significant advantages over the existing mechanisms the OS already supports (Intel Memory Protection Keys and Extended Page Tables). Due to the fine-grained memory protection capabilities offer, safety will be increased by allowing to share only the minimum amount of data for cross-compartment communications. Such communications' performance should also be enhanced compared to solutions based on data copy. Capabilities will also allow FlexOS to scale to a high number of compartments, something not possible with the currently supported mechanisms, for architectural (MPK) or performance (EPT) reasons.

A first step towards porting FlexOS to Morello will be to port FlexOS' basis, Unikraft, to the platform. Unikraft is a high-performance/low latency unikernel targeting cloud and edge applications. Unikraft's performance benefits come from the fact that, following the principle from the unikernel OS model, kernel and application code share a single, completely unprotected, address space. This obviously raises security concerns. Porting Unikraft to Morello gives us the unique opportunity to study bringing back safety into unikernels while maintaining the high degree of performance offered by that OS model. We plan to achieve that using the safety benefits brought by capabilities to legacy programming languages (Unikraft is written in C) through pure and/or hybrid capabilities.

Finally, we aim to explore advanced uses of the compartmentalization and safety features of capabilities along two possible research avenues: 1) the use of compartmentalization as provided by FlexOS to allow incremental port of some/all of OS/user components to Morello's pure capability model; 2) vertical compartmentalization through capabilities in FlexOS in order to address confused deputies, a type of vulnerability that is becoming increasingly problematic in today's compartmentalised software.

## Contact

- [Pierre Olivier](https://sites.google.com/view/pierreolivier), The University of Manchester `pierre dot olivier at manchester dot ac dot uk`

* * *

<p align="center">
  <img src="assets/uom-logo.png" height=150 style="margin:20px" />
  <img src="assets/ukri-logo.png" height=150 />
</p>
