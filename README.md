# Background and Motivation

In many scenarios, particularly with the rise of Trusted Execution Environments (TEEs) and the increasing security demands for IoT devices and confidential workloads, it's crucial to ensure that the peer's state is as expected, in addition to conventional authentication (verification of identity).

Remote attestation ([RFC9334](https://datatracker.ietf.org/doc/rfc9334/)) addresses this by allowing an entity to produce verifiable Evidence about its current state - such as proving that its software and firmware haven't been tampered with, that secure boot is enabled, or that cryptographic keys are securely stored within a hardware-protected environment.

This provides a much stronger assurance of trustworthiness, helping to prevent attacks that might compromise a system even if its traditional credentials remain valid, and enables authorization policies based on richer security signals.

To address this need for enhanced, verifiable trustworthiness, this WG will deliver a Standards Track solution based on a post-handshake exchange for TLS that enables the attestation of one or both TLS endpoints.

Such a mechanism would allow an entity to produce (fresh) Evidence or an Attestation Result about itself for another party to evaluate.

This effort will focus on leveraging the (D)TLS handshake protocol as-is. It will also leverage the existing RATS toolbox to ensure interoperability with existing and future attestation technologies.

# Goals

This working group has a narrow focus: to produce a single document specifying a post-handshake exchange for TLS that provides attestation of one or both TLS endpoints.

More specifically:
* The protocol should be agnostic to remote attestation technologies.
* TLS 1.3 handshake protocol should be used as-is, leveraging its existing deployment and security guarantees, including formal validation.
* The protocol may specify negotiation mechanisms within the initial TLS handshake.
* The protocol must allow per-session freshness.

The working group will not extend TLS or create new remote attestation technologies or cryptographic protocol mechanisms.

The working group will engage with the research community on the formal analysis of the protocol artefacts in parallel with the specification work.

We propose to use [Exported Authenticators (RFC9261)](https://datatracker.ietf.org/doc/rfc9261/) as the post-handshake mechanism and [Conceptual Message Wrapper (CMW)](https://datatracker.ietf.org/doc/draft-ietf-rats-msg-wrap/) as the format for the attestation credential. 

# Dependencies and Liaisons

The working group will keep the TLS and RATS working groups informed of its activities by presenting updates at their meetings and requesting reviews.

Regarding the formal analysis aspects, the working group will similarly engage with the UFM research group.

# Program of Work

TBD.
