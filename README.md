# [SciPy 2021](https://www.scipy2021.scipy.org/) Submission Instructions

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

## Title and Abstract
> The title and the abstract should be entered as plain text, they should not contain HTML elements.

### Title

pyhf: a pure Python statistical fitting library with tensors and autograd

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

Though pyhf is a tool from high energy physics, out of the available mini-symposium at SciPy 2021 it best fits under Astronomy and Astrophysics, as the techniques can be of general interest to the broader physics community.

- pyhf on GitHub: https://github.com/scikit-hep/pyhf
- pyhf on PyPI: https://pypi.org/project/pyhf/
- pyhf documentation: https://scikit-hep.org/pyhf/
- List of talks given on pyhf: https://scikit-hep.org/pyhf/talks.html
   - Most recent and relevant: Matthew Feickert. pyhf: pure-Python implementation of HistFactory. PyHEP 2019 Workshop, October 2019. https://indico.cern.ch/event/833895/contributions/3577824/
- List of scientific publications that have used pyhf: https://scikit-hep.org/pyhf/citations.html

> Word count including hyperlinks: 508

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

## Other Information and Files

### Please select the track or mini-symposium for your submission.
Select the category below that best fit your topic.

- [ ] General
- [ ] High Performance Python
- [ ] Machine Learning and Data Science
- [x] Astronomy and Astrophysics
- [ ] Biology and Bioinformatics
- [ ] Materials Science
- [ ] Earth, Ocean, Geo and Atmospheric Science
- [ ] SciPy Tools (5 minute mini presentations)
- [ ] Maintainers Track (Submissions will be shared with Maintainer Track Co-Chairs, but will not be part of the formal review process.

### Short Summary
> A brief description which will appear in the online program and give attendees a basic sense of your talk.
> This should be around 100 words or less

High Energy Physics analyses are performed with statistical computations to determine the compatibility of the reported results with the existing Standard Model.
In many cases, a binned, asymptotic likelihood fit is performed following a mathematical p.d.f. template called HistFactory.
The pyhf library is a pure-Python implementation of that statistical model for multi-bin histogram-based analysis and asymptotic interval estimation.
pyhf supports modern computational graph libraries such as TensorFlow and PyTorch to make use of features such as auto-differentiation and GPU acceleration.
Additionally, pyhf's JSON model specification has enabled the first open publication of full likelihoods from an LHC experiment.

> Word count: 98

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
- [ ] High Performance Python
- [x] Data Driven Discoveries
- [x] Astronomy and Astrophysics
- [ ] Biology and Bioinformatics
- [ ] Materials Science
- [ ] Earth, Ocean, Geo and Atmospheric Science

### Paper (optional).
Upload your paper (optional).
The paper must be in PDF format (file extension .pdf)
