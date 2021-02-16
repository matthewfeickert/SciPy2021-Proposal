# [SciPy 2021](https://www.scipy2021.scipy.org/) Submission Instructions

## Track

- [ ] SciPy 2021 Tutorials
- [ ] Data Visualization and Image Processing
- [ ] Scientific Applications of Machine Learning & Data Science
- [ ] Computational Social Science and Digital Humanities
- [ ] Biology and Neuroscience
- [ ] Earth, Ocean, Geo, & Atmospheric Science
- [ ] General
- [ ] Maintainers Track
- [x] Physics & Astronomy

## Author 1

- First Name: Matthew
- Last Name: Feickert
- Email: matthew.feickert at-no-spam cern.ch
- Country: United States
- Organization: University of Illinois at Urbana-Champaign
- Web page: http://www.matthewfeickert.com/
- Corresponding Author: Yes

## Author 2

- First Name: Lukas
- Last Name: Heinrich
- Email: lukas.heinrich at-no-spam cern.ch
- Country: Germany
- Organization: CERN
- Web page: http://www.lukasheinrich.com/
- Corresponding Author: No

## Author 3

- First Name: Giordon
- Last Name: Stark
- Email: gstark at-no-spam cern.ch
- Country: United States
- Organization: Santa Cruz Institute for Particle Physics, UC Santa Cruz
- Web page: https://giordonstark.com/?utm_source=scipy&utm_medium=proposal&utm_campaign=2021
- Corresponding Author: No

## Author 4

- First Name: Ben
- Last Name: Galewsky
- Email: bengal1 at-no-spam illinois.edu
- Country: United States
- Organization: National Center for Supercomputing Applications
- Web page: https://bengalewsky.github.io/
- Corresponding Author: No

## Title and Abstract
> The title and the abstract should be entered as plain text, they should not contain HTML elements.

### Title

Distributed statistical inference with pyhf powered by funcX

### Abstract

> c.f. the [Planning for your proposal submission?](https://github.com/matthewfeickert/SciPy2021-Proposal/blob/master/info_page.md#planning-for-your-proposal-submission) information page

> Your placement in the program will be based on reviews of your abstract.
This should be a roughly 500 word outline of your presentation.
This outline should concisely describe software of interest to the SciPy community, tools or techniques for more effective computing, or how scientific Python was applied to solve a research problem.
A traditional background/motivation, methods, results, and conclusion structure is encouraged but not required.
Links to project websites, source code repositories, figures, full papers, and evidence of public speaking ability are encouraged.

#### Introduction and Motivation

Researchers in High Energy Physics (HEP) and other fields are encouraged by their funding bodies to take advantage of the High Performance Computing (HPC) facilities constructed at various institutions.
These facilities include capable machines such as Theta at Argonne National Laboratory with 280,000 cores and 192 hardware-accelerated GPUs.
While powerful, these architectures do not easily support the Python compute model.
Users must construct batch jobs and submit them to a queue for execution when compute time is available.
The results are stored on the file system and must be stitched back together once all of the jobs have completed.
On many of these systems, Python tooling lags the current state of the art and configuring modern Python libraries to use HPCs can be a tedious task and require expertise.

In HEP a core component of analysis of data collected at the Large Hadron Collider (LHC) is performing statistical inference for binned models to extract physics information.
The fitting of multiple different hypotheses for new physics signatures (signals) is a computational problem that lends itself easily to parallelization, but is hampered on HPC environments by the additional tooling overhead required, which can be very difficult to master.
The statistical fitting tools used in HEP have traditionally been implemented in C++, but in recent years pyhf, a pure-Python library with automatic differentiation and hardware acceleration, has grown in use for the statistical inference problems described.
Through use of funcX, a pure-Python high performance function serving system designed to orchestrate scientific workloads across heterogeneous computing resources, pyhf can be used as a highly scalable (fitting) function as a service (FaaS) on HPCs.


#### Combined performance gain

Through adoption of open source "tensor" computational Python libraries, pyhf is able to leverage tensor calculations to outperform the traditional C++ implementations on data from real LHC analyses.
funcX is able to create and register a service endpoint on HPC systems that interfaces with native schedulers.
End users are able to register functions through a Python API and then scalebly execute workloads, with demonstrated use of scaling to more than 100,000 workers.
We have demonstrated use of funcX to orchestrate pyhf to simultaneously fit 125 signal hypotheses in the parameter space of a published LHC physics analysis with a wall time of under 3 minutes.
The combination of pyhf and funcX reduces a common problem in HEP analyses that would traditionally take multiple hours and bespoke scheduling to an on-demand (fitting) FaaS, offering reduced time to insight and inference.

#### Conclusions

Through the combined use of the pure-Python libraries funcX and pyhf, we have demonstrated the ability to parallelize and accelerate statistical inference of physics analyses on HPC systems through a FaaS solution.

#### Audience

- Who is the intended audience for the talk?

This talk would be of particular interest to scientists and engineers who are looking to leverage HPC solutions for their analysis workflow while simultaneously exploiting the extensive tooling of the scientific Python ecosystem.

- What, specifically, will attendees learn from the talk?

Regardless of audience background, they will learn how to extend the normal scientific workflow in Python to HPC solutions using FaaS.

#### Notes

- pyhf on GitHub: https://github.com/scikit-hep/pyhf
- pyhf on PyPI: https://pypi.org/project/pyhf/
- pyhf documentation: https://pyhf.readthedocs.io/
- List of talks given on pyhf: https://pyhf.readthedocs.io/en/v0.6.0/outreach.html#presentations
   - Most recent and relevant: Matthew Feickert. pyhf: a pure Python statistical fitting library with tensors and autograd. SciPy 2020, July 2020. https://doi.org/10.25080/Majora-342d178e-023
- List of scientific publications that have used pyhf: https://pyhf.readthedocs.io/en/v0.6.0/citations.html

- funcX on GitHub: https://github.com/funcx-faas/funcx
- funcX on PyPI: https://pypi.org/project/funcx/
- funcX documentation: https://funcx.readthedocs.io/en/latest/index.html
- List of talks given on funcX: https://funcx.org/publications.html
   - Most relevant: K. Chard. funcX: A Federated Function Serving Fabric for Science https://funcx.org/presentations/20-8-funcX-Linea.pdf
- List of scientific publications that have used funcX: https://funcx.org/publications.html

- Talks related to pyhf and funcX:
   - Matthew Feickert. Fitting and Statistical Inference as a Service, IRIS-HEP Workshop on Portable Inference, December 2020. https://indico.cern.ch/event/972791/contributions/4121109/

> Word count excluding Notes section: 520

## Keywords
> Type a list of keywords (also known as key phrases or key terms), one per line to characterize your submission. You should specify at least three keywords.

- Physics
- Statistics
- Fitting
- Optimization
- Auto-Differentiation
- funcX
- Functions as a Service
- High Performance Computing

## Other Information and Files

### Short Summary
> A brief description which will appear in the online program and give attendees a basic sense of your talk.
> This should be around 100 words or less

In High Energy Physics (HEP) there is motivation to perform statistical inference required for analysis of data from the Large Hadron Collider on High Performance Computing environments, which can pose problems with orchestration and efficient scheduling.
The combination of the pure-Python libraries pyhf and funcX reduces the common problem in HEP analyses of performing statistical inference with binned models, that would traditionally take multiple hours and bespoke scheduling, to an on-demand (fitting) function as a service that can scalable execute across workers in just a few minutes, offering reduced time to insight and inference.

> Word count: 95

### Type of Submission.
Please indicate whether you would like to be considered for a talk slot or poster slot.
Please note that talks that are not accepted are automatically considered for a poster slot.

- [x] Talk
- [ ] Poster

### Are you (the submitting author) interested in serving on the program committee?.
Program committee members review submissions for inclusion in the program.

The associated workload is fairly light; last year, each review board member reviewed approximately seven 150 word abstracts, approximately a 2-3 hour time commitment.

If you would like to join the program committee, please select the topics below that you feel comfortable reviewing.
If you do not wish to join, leave the below checkboxes blank.

Participation will have no impact on whether or not your submission is accepted.

- [x] General
- [ ] Data Visualization and Image Processing
- [x] Scientific Applications of Machine Learning and Data Science
- [x] Physics and Astronomy
- [ ] Biology and Neuroscience
- [ ] Computational Social Science and Digital Humanities
- [ ] Earth, Ocean, Geo and Atmospheric Science

### Paper (optional).
Upload your paper (optional).
The paper must be in PDF format (file extension .pdf)
