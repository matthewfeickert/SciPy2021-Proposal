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

**TODO: TITLE**

### Abstract

> c.f. the [Planning for your proposal submission?](https://github.com/matthewfeickert/SciPy2021-Proposal/blob/master/info_page.md#planning-for-your-proposal-submission) information page

> Your placement in the program will be based on reviews of your abstract.
This should be a roughly 500 word outline of your presentation.
This outline should concisely describe software of interest to the SciPy community, tools or techniques for more effective computing, or how scientific Python was applied to solve a research problem.
A traditional background/motivation, methods, results, and conclusion structure is encouraged but not required.
Links to project websites, source code repositories, figures, full papers, and evidence of public speaking ability are encouraged.

#### Introduction and Motivation

In experimental high energy physics (HEP), statistical fitting tools have been implemented almost entirely in C++.
One common example used by experimentalists at CERN uses the "HistFactory" p.d.f. template.
Prominently used in the 2012 discovery of the Higgs boson by the ATLAS and CMS collaborations, the p.d.f. template has only been implemented within the C++ based ROOT framework, maintained by CERN.
pyhf is a pure-Python implementation of that statistical model for multi-bin histogram-based analysis with asymptotic interval estimation, and part of the Scikit-HEP project (https://scikit-hep.org/) ecosystem.
pyhf supports modern computational graph libraries as computational backends in order to make use of features such as auto-differentiation and GPU acceleration.
Additionally, the statistical models are defined in a declarative JSON schema, readily enabling preservation and distribution through services such as the Durham High-Energy Physics Database (HEPData) (https://www.hepdata.net/).

#### Performance gain through tensorization

Through adoption of open source "tensor" computational Python libraries, pyhf decreases the abstractions between a physicist performing an analysis and the statistical modeling without sacrificing computational speed.
In fact, by taking advantage of tensor calculations, pyhf outperforms the traditional C++ implementations on data from real LHC analyses.
pyhf's default computational backend is built from NumPy and SciPy, and supports TensorFlow, PyTorch, and JAX as alternative backend choices.
These alternative backends support hardware acceleration on GPUs, and in the case of JAX JIT compilation, as well as auto-differentiation allowing for calculating the full gradient of the likelihood function --- all significantly speeding up fits.

#### Model specification

pyhf's model specification is in JSON as it offers long term support, is human and machine readable, and is highly compressible.
All of these benefits make it ideal for analysis archival and, since almost every language has a JSON parser, allows for the model specification to be independent of the HistFactory implementation language.

#### Conclusions

pyhf is the first pure-Python implementation of the HistFactory statistical model from HEP.
It is being used by experimentalists and theorists analyzing LHC data and is enabling open publication of LHC experiment data products for the first time.

#### Audience

- Who is the intended audience for the talk?

This talk would be of particular interest to scientists, engineers, and statisticians (both Frequentist and Bayesian inference can be performed with pyhf) who are looking to use machine learning frameworks for statistical analysis in Python.

- What, specifically, will attendees learn from the talk?

Regardless of audience background, they will see how they can use modern machine learning frameworks to accelerate statistical analysis in Python.

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

> Word count including hyperlinks: ???

## Keywords
> Type a list of keywords (also known as key phrases or key terms), one per line to characterize your submission. You should specify at least three keywords.

- Physics
- Statistics
- Fitting
- SciPy
- NumPy
- TensorFlow
- PyTorch
- JAX
- Auto-Differentiation
- funcX

## Other Information and Files

### Short Summary
> A brief description which will appear in the online program and give attendees a basic sense of your talk.
> This should be around 100 words or less

**TODO**

> Word count: ???

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
