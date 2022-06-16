---
tags: [journal]
---

## Thursday, June 16, 2022

-> Yesterday, I've read a paper titled "Web Identity Translator. Behavioral Advertising and Identity Privacy with WIT". It's a work in the domain of [online privacy](../pages/online%20privacy.md) in the context of online advertising. 

### Distractors

- [Incognito: A Method for Obfuscating Web Data](https://api.semanticscholar.org/CorpusID:4900427)
- [Anonymity Online – Current Solutions and Challenges](https://hal.inria.fr/hal-01883626/document)

---

## Tuesday, June 14, 2022

I'm dealing with a case where read data set is a snapshot of a current state. Most operations work on the latest snapshot. However, there is an operation that computes a difference between two versions of the data set. I've decided to use Hive partitioning and set the snapshot version as the partition key.

### Today's scattered thoughts

- Read [System Design Interview Questions](https://www.interviewbit.com/system-design-interview-questions/)
- CSAIL - what are they doing? what are they publishing? should follow?
- programmatic guaranteed deals - how to ensure that that the guaranteed cap of impressions will be delivered? what if there is no forecast or reliable forecast?

## Monday, June 13, 2022

Latest months I struggle with organizing my work. This struggle causes terrible ineffectiveness of my time spent at work. At first, I have a problem with clarifying what topic is important and why. Even if I choose one, I have a difficulty with defining milestones or steps to proceed. In effect, I feel like I am not doing anything important or valuable for anyone. I don't see any work progress, nor outcomes I would like to achieve. Everything looks to me as a total mess. No goal. No strategy. No value. Frustration. Anger. Mental breakdown.

However, it should be simple to put all the things on the right track. In my opinion the creative work in technology always was like: reading, writing, learning, coding, and adjusting the perspective of what's *the next big thing* (at least for myself od my company).

### Today's implementation work

- [Budget pacing](../projects/Budget%20pacing.md)
	- After introducing of the IO managers (Dagster) into the project, I must rewrite the results analysis. Today I started with the spent budget plots.

### Today's writing

- [Dagster](../pages/Dagster.md)

### Today's distracting thoughts

 - Test the [Singer](https://www.singer.io/), at least the taps to the services I have access to. Ask teams about services they must integrate with in projects. Check with what tools can it be integrated, e.g. with workflow orchestrator.
 - [Kubernetes feature gates](https://kubernetes.io/docs/reference/command-line-tools-reference/feature-gates/) and how to enable them in [K3s](https://forums.rancher.com/t/enable-feature-flags-on-k3s/20350)
