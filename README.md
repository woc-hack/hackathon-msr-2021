# MSR 2021 Hackathon

## 1. Call for Participation

The proliferation of open source software (OSS) development has
created novel and massive software supply chains and ecosystems that
require non-traditional approaches of software development. Even the
approaches that fared well in the earlier stages of open source
development are challenged by the sheer scale of the present open
source ecosystem, the complexity of dependencies among projects, and
the lack of effective means of establishing trust essential for
frictionless collaboration - a cornerstone of OSS.

World of Code (WoC) is an attempt to cross-reference all OSS
projects and represents over 120M git repositories from GitHub, GitLab,
BitBucket, etc. with over 2B git commits (42M authors), 8B
blobs, and 8.3B trees. The content of these objects is augmented via
cross-referencing (a graph). For example, all commits that have
created a specific blob, all repositories where a specific blob or a
specific commit resides in, all commits for a specified author ID,
and other maps that are impossible to compute without having an
almost complete set of repositories.

Hackathons are effective ways to explore research and product ideas
by teaming up with others on intense but limited in duration
tasks. We propose WoC online hackathon to explore problems and
solutions in open source software development that either apply at a
global scale or require measurement approaches done at that
scale. Examples for these are any measurements such as complete OSS
activities of developers, complete downstream dependencies of a
project, or the provenance of a source code file.

The event will provide activities typical of the in-person hackathon
virtually. For example, defining research questions, forming teams,
and scoping problems. Organizers will provide advice on
the best ways to conduct data processing and improve performance.
The hackathon will also provide the opportunity for participants to
work with world-class researchers on relevant problems and research
questions.

Please join if you are concerned about the continued health of open
source software and would like to make a difference! This applies to
anyone trying to support industry and educational use of open
source, such as assessing risks, effectiveness and spread of
tutorials, frameworks, tools, and practices. Questions related to
obtaining large representative samples of data for software
engineering research are equally welcome.

The teams selected by the PC will have the opportunity to publish
the description of their work at MSR'2021. Previous WoC hackathon
resulted in four publications at MSR'2020.

Any topics related to doing research, building tools, or improving
infrastructure that supports global OSS development, helps industry
use OSS, or educational/training aspects related to work in this
giant network, are within the scope of the hackathon. For example,
- Applications that support finding suitable code, people, projects,
or bugs and/or model the social and technical networks and their
evolution.
- Applications that increase transparency by making it easier to
become a contributor or that helps maintainers zero in on most
relevant contributions.
- Applications that increase understanding of software supply chains
and ecosystem: how and why they function and how to manage risks,
especially as related to industry use of OSS.
- Any infrastructure work that does data fusion or data quality
improvements, such as leveraging all open source data sources in WoC
resource and beyond.
- Approaches to better collect data increase the coverage or encourage
outside contributions.


## 2. Key Dates

* The project ideas from participants will be collected until
  October 15, 2020.

* The date for hackathon itself will be arranged by conducting the
  survey of the project idea submitters and will be conducted in
  November or December of 2020.

## 3. The Process

An online hackathon for researchers who would like to team up with
others on crucial problems for supporting Open Source
Software. Organizers will provide training for World of Code
resource that supports global measurement of OSS in the form of a
webinar prior to the event.

The event will provide activities typical of the in-person hackathon
virtually. For example, defining research questions, forming teams,
scoping problems. This will be done while also providing advice on
the best ways to conduct data processing and improve performance.

Organizers will provide support in the form of mentors that can help
with technical issues. The hackathon will also provide the
opportunity for participants to work with world-class researchers on
relevant problems and research questions.

The preparation will involve team forming activities and a set of
online tutorials during which we will walk MSR Hackathon
participants through key functionality.
 
A dedicated (issue tracker) to answer questions and solve issues for
the participants of MSR Hackathon will also be available.  Slack and
Zoom will be suggested as the main means of communication during the
hackathon between teams, mentors and organizers.  A dedicated Zoom
room will be provided for each team during the entire duration of
the event.

The results of the hackathon will be evaluated by the Hackathon
Evaluation Committee based on the originality of the idea, potential
impact of the proposed solution, and the sophistication of the
artifacts produced during the hackathon.

The winning teams will have an option to present their results at a
special session of Mining Software Repositories conference 2021.

## 4. World of Code Resource for Hackathon

WoC version R represents 123M git repositories from GitHub, GitLab,
BitBucket, etc. based on updates/new repositories identified on Mar
7, 2020, and retrieved by Mar 28.  It has 2B git commits (42M
authors), 8B blobs, and 8.3B trees. The content of these objects is
augmented via cross-referencing (a graph) for immediate access to
all object references associated with any specific object. For
example, all commits that have created a specific blob, all
repositories where a specific blob or a specific commit resides in,
all commits for a specified author ID, the child commits of a
specific commit, and other maps that are impossible to compute
without complete data.

Developers often have multiple commit author IDs. WoC solves this
problem via a map that associates each author ID with imputed
developer identity . Some of these are actually bots .

With many repositories being clones or forks, WoC for each repo also
provides an estimated project identity for each repository . This
results in 69M independent projects.

Time-based selection of commits and selection of projects and
authors based on the characteristics of files and activities
associated with them is also provided.

WoC pre-calculates basic summaries for each blob by running ctags
and stores the results as well as diffs for all 2B commits.
Finally, WoC provides blob to import/include/use statements parsed
from blobs in 17 programming languages.

### Access

Due to its large size, WoC provides ways to easily access, sample,
and analyze the data based on all the cross-referencing
capabilities. Shell, Python, and Perl API can be use on WoC servers
via ssh (high performance) and REST APIs for web access.  Users need
to fill in a short web form for ssh access.

### Participant needs                        

Participants who are comfortable using terminal would benefit from
high performance of ssh access where two simple shell commands
showCnt and getValues can be composed with regular shell commands
into an arbitrarily complex analysis as described in the
tutorial. Participants who disdain terminal can use Python in
Jupyter notebooks on WoC servers or run Jupyter notebooks on
participants' computers and access WoC via REST APIs .  The primary
focus of WoC is to provide cross-referencing and completeness of the
coverage of the git objects from public repositories. Participants
will be responsible for integration of WoC data with other types of
data they may need: e.g., issue metadata from GHtorrent, code
parsing, statistical modeling, and and other types of data and
analysis.

### The research questions

The purpose of WoC is to enable answering questions that can not be
answered without the completeness and cross-referencing of public
git data. Research on networks of developers, code, and API's would
be benefit the most. For example, questions that require the
measurement of activity of the entire OSS at a particular slice of
time, identifying all commits/repositories/blobs/developers
associated with a specific developer/blob/API, finding all child
commits of any commit, or finding all forks/clones of a
repository. Simple tasks like finding all commits/blobs associated
with a repository are supported but do not require WoC, as ``git
clone'' would suffice. WoC can be used for representative sampling
of the developers and projects by developer and project network
properties .  Such complete picture allows to go past MSR analyses
limited by data filtered on the set of non-representative projects
and, therefore, unable to capture the full scope of developer
activity, code reuse, or API usage.  Mining questions might involve
improving quality of WoC data, its performance, ways to link to
other datasets. WoC use examples are in and in publications in
Appendix III.  The evolution of open source software, developer and
project ecosystems, past and current trends, counting and
summarizing developers, projects, the source code, and the dynamics
of developer and code movements across entire OSS ecosystem are
examples of research questions that could not be answered without
WoC. Answers to these questions have major practical implications
for developers and industry alike: will a library becomes obsolete?
Do we have any open source code?

### Sample data

Since sampling large graphs is difficult, we provide a
Jupyter notebook that investigates blobs/projects/authors associated
with a Common Vulnerability and Exposure (CVE).


## References

[CFP](https://github.com/woc-hack/msr-hackathon/blob/master/MSR-Hack-CFP.pdf)

[WoC Tutorial](https://github.com/woc-hack/tutorial/blob/master/README.md)

[CVE Dataset Notebook](https://github.com/woc-hack/msr-hackathon/blob/master/CVEJupyter.ipynb)

[REST Notebook](https://github.com/woc-hack/msr-hackathon/blob/master/RESTJupyter.ipynb)

[How to do sampling](https://github.com/woc-hack/msr-hackathon/blob/master/sampling-resource.md)

[Python Notebook](https://github.com/woc-hack/msr-hackathon/blob/master/PYJupyter.ipynb)
