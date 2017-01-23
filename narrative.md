## Progress

*Describe your project's progress in the last year. Please reference your initial project objectives when possible.*

Award purpose:

>In support of demonstrating the high level of scientific impact
>that data scientists deliver through their focus on
>interdisciplinary data-driven research; funds from this award will
>be used to better understand gene function in non-model organisms
>through the development of new workflows and better data sharing
>technology for large-scale data analysis.

The second year of this award saw substantial progress towards
outlining a strategy towards these ends, and developing specific
foundational technologies and software.  (The first year of this award
was dominated by the process of moving to UC Davis and recruiting
postdocs to my new lab!)  Since last report, three new postdocs
(Daniel Standage, Harriet Alexander, and Phillip Brooks) have joined,
and all are working on DDD-related projects.

We are now moving forward on several fronts:

* we have a transcriptomics team working on reanalysis of 700
  transcriptomes (MMETSP project, Lisa Cohen and Harriet Alexander)
  using technology developed by Camille Scott (dammit and shmlast).
  In addition to the primary products (new & better assemblies), we
  have a robust, quality-controlled open and canonical de novo
  assembly and annotation pipeline that can be applied to any
  eukaryotic RNAseq data set.

* a metagenomics group (Sherine Awad, Phil Brooks) is moving towards
  the same goal in metagenomics data analysis.
  
* our distributed/scalability tiger team (Luiz Irber) is working to
  build distributed indices of MinHash sketches to make it possible to
  find relevant data sets and analyses in public databases.  As part
  of this Luiz is building a massively scalable indexing
  infrastructure that closely resembles a botnet.
  
* our core software development efforts are proceeding again, with
  Daniel Standage leading khmer development and a consultant (Tim Head)
  contributing to development, code review, and testing.

* while doing all of this, we continue to explore the landscape of
  tools and resources around notions of openness, repeatability,
  decentralization and distribution, and community engagement.  In
  addition to my own robust social media presence, an analysis of
  challenges in doing large scale data reanalysis on a small lab
  budget will be submitted along with the primary MMETSP reanalysis
  paper.

* an important component of all our work is our teaching and training
  effort, aimed at building a local community of practice around
  data-driven discovery while engaging with the global community being
  nucleated by the Data Science Environments and Data Carpentry.
  Towards this end we have run dozens of workshops in the past two
  years and plan to considerably scale up in the summer of 2017.
  
It's hard to predict where we will end up but I'm enjoying the ride,
and in the meantime we are producing useful software products and
doing interesting analyses.

## Awareness and recognition

*Describe evidence of awareness/recognition of you, your projects, and/or your lab members.*

I continue to be recognized as a source of informed opinion about
issues of open science, computational infrastructure, scientific
software engineering, and repeatability/reproducibility.  The primary
broadcast medium for these opinions is social media, with my blog and
Twitter accounts.  As evidence of engagement, my blog sees about
90,000 page views a year, and gathers about 200 comments per year;
I don't know how to summarize my Twitter traffic.  It seems likely
that many of my invitations and advisory board memberships come from
my social media presence, as I have mostly avoided publishing opinion
pieces or review articles in traditional locations.  I also routinely
provide background information and give interviews to science
journalists.

More than just me, the lab is increasingly being recognized as a
source of expertise in software development, data-intensive research,
and infrastructure.  For example, Luiz did a tutorial on Docker at
Supercomputing 2016; Harriet and Daniel both participated in a
national Plant Biology computing infrastructure visioning workshop;
and Harriet has participated in several additional visioning workshops
and grant review panels.

### Help requested

#### Compute infrastructure

There is a general confusion and lack of clarity around the
computational infrastructure needs of Data Driven Discovery, and where
and how to meet them.  This includes just-in-time resources for
training, long term storage of large datasets, "scale out" technology
options, good-enough practice in making use of the options, and
funding/support for large scale compute and storage.  (This is also
alluded to in Casey Greene's report.)  

We are working on a local (UC Davis School of Vet Med) solution to
container hosting, and also starting to interact more closely with
NSF's JetStream, as two possible solutions for our lab.

But, more generally, I don't know what a sustainable option is here.
It seems like a good opportunity for some brainstorming.

#### Learning about deep learning

I need to know more about deep learning, and gain some hands on
experience.  More, I would like to be able to engage closely with
experts in order to figure out what will and won't work. People in my
lab are also interested in this. Where do we go?
