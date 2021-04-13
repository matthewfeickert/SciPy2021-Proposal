# Talk Proposal Reviewer Comments

The talk submission "Distributed statistical inference with pyhf powered by funcX" was selected for presentation at SciPy 2021 (in the Physics and Astronomy mini-symposia).

SciPy practices a double-open review system.
The following are the reviews for the submission:

- **SUBMISSION:** 89
- **TITLE:** Distributed statistical inference with pyhf powered by funcX
- **AUTHORS:** Matthew Feickert, Lukas Heinrich, Giordon Stark, and Ben Galewsky

## Review 1

**Overall evaluation:** 3 (strong accept)

### Overall evaluation

NB: my domain of expertise was astronomy.

This talk would introduce:

1) pyhf, a library for simultaneous fitting of many models to binned data from high-energy physics experiments
2) funcX, a library that eases interactions with queue-based HPC systems

Here are my answers to the review questions on the scipy conference website:

> Is the abstract clear?

Yes. No jargon was used; I didn't need expertise in HEP.

> Is the abstract complete?

Yes.

> Is the abstract compelling?

Yes. I would attend this talk (and probably will).

> How relevant, immediately useful, and novel is the topic?

I probably could have used funcX during my first postdoc, which is to say that managing queue-scheduled computations with Python is immediately useful.
The abstract makes the problem seem like low-hanging fruit for which the solution will be applicable to a large audience.

## Review 2

**Overall evaluation:** 2 (accept)

### Overall evaluation

This talk focuses on making making Python-based calculations easier on HPC clusters.
While the application in the proposal is high energy physics, I gather that it has potential applications in other domains.
As long as proposers emphasize that broader applicability I think the talk will generate reasonably broad interest.
There was considerable interest at SciPy 2020 in HPC and imagine that will be true again this year.
The talk the proposers gave at SciPy 2020 was good -- I am confident that this will be also.

## Review 3

**Overall evaluation:** 2 (accept)

### Overall evaluation

The authors present an alternative approach to perform statistical inference on HPC center based on a "function as a service" (FaaS) approach.
The approach of developing services is already well established in the private sector (such as platform as a service in cloud computing) and has the potential to simplify the interaction process with large HPC facilities for scientists while allowing for careful optimizations by the programmers.

The abstract is laid carefully and properly introduces all the concepts required for its understanding by a broad audience that extends outside of physics and astronomy.
The abstract clearly states how it relates to the existing ecosystem, what novelty it brings and how it is structured.
Finally, the "Combined Performance Gain" paragraph provides compelling evidence of the benefits of the FaaS approach and of the performance of pyhf.

The project has already been presented at past Scipy conferences.
Unfortunately, it is not obvious from the abstract how this talk would distinguish itself from past ones.
Provided the authors manage to present a different perspective or new features compared to last year (and the activity on the public Github repository are encouraging in that direction), I am confident the talk would however be of high interest.

Overall, this is a very good abstract that should be of high interest to the SciPy community.
I am  in favor of accepting it.

## Review 4

**Overall evaluation:** 3 (strong accept)

### Overall evaluation

The talk discusses how Physics High Performance Computing could take advantage from a Function as a Service infrastructure implemented via a pure-Python library.
The abstract is well detailed and clearly identifies the objectives of the presentation.
The described tools are well referenced  in the abstract and documented, proving a high level of maturity.
The title of the presentation could benefit of a small reformulation for non-expert audience.
HEP applications have been early users of HPC and the way they are ported on new architectures (GPU) and tools (Python) is a very interesting use case for the scipy community.

## Review 5

**Overall evaluation:** 3 (strong accept)

### Overall evaluation

The authors used a combination of funcX and pyhf to solve statistical inference problems applied to high energy physics.
The abstract is very clear and complete.
Although it seems that the goal of the talk is not intended for the whole audience, some information will be useful for all.
In particular, and as the authors mention, "regardless of audience background, they will learn how to extend the normal scientific workflow in Python to HPC solutions using FaaS".

## Review 6

**Overall evaluation:** 3 (strong accept)

### Overall evaluation
