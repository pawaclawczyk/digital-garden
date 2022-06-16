---
tags: [concept]
---

# Online privacy

## Privacy proxy

The [[privacy proxy]] concept includes following techniques improving user's privacy:
- obfuscating of the IP address #confirm 
- [[identifiers translation]] with privacy controls and intervention algorithms

### *Web Identity Translator: Behavioral Advertising and Identity Privacy with WIT* (2015)

The article proposes use of a proxy between user's device and tracking server.

In standard situation, without a proxy, a user identifier is sent between the device and the server. With use of [[third-party cookies]] (other options are [[fingerprinting]] #confirm , [[CNAME cloaking]] #confirm ), the tracking service can trace user browsing history, which can be used to build a [[user signature]]. That, even if the identifier is changed, the new signature can be matched to the past one. The proxy task is mapping a tracking (public) identifier to a private identifier sent further to the device, and reverse mapping in the opposite direction (operation similar to [[NAT]]). Mapping identifiers alone won't introduce privacy qualities to the process, especially if the public identifier is stable across multiple domains, so the authors propose a way to protect user's identity from being matched against its past signatures. In the first phase, the proxy builds user signature using the private identifier. In the next phase, this signature is used to test whether user's signature built using public identifier is in enough distance from the real user signature, in other words, the signature does not match the signature that would be build if there will be no proxy. In order to preserve the distance, the proxy can intervene in the mapping process; it can drop the public identifier, so a new would be assigned, inject user's history elements that make him look similar to other users (*history padding*), swap the identifier with another user identifier (*cookie swap*). The articles defines a similarity measure and similarity rank used to detect when the proxy should intervene.

The user's browsing history is a foundation of the [[online behavioral advertising]]. The authors checked (not very seriously) the impact of the proxy interventions on the assigned interest tags.

[Semantic Scholar](https://api.semanticscholar.org/CorpusID:19026658)
