## Moore-supported projects that I'd like to highlight:

### Re-analyzing the Marine Microbial Eukaryotic Transcriptome Sequencing Project

Ably driven forward by Lisa Cohen (graduate student) and Harriet
Alexander (postdoc), we are re-analyzing the ~700 MMETSP transcriptome
data sets generated about 5 years ago by the Moore Foundation.

Major highlights:

* this effort should dramatically improve usability of these data sets
  by the field, both now (updated annotations, expression) and in the
  future (because we can update the annotations fairly easily).

* we have a single script that will trim, assemble, annotate, and
  calculate expression levels for ~arbitrary numbers of RNAseq
  samples.

* the reanalysis effort has led to a lot of insight into the problems
  of bio(medical) data reanalysis and sharing, which Harriet is
  writing up as a companion "op-ed" piece to Lisa's paper.

* the community reaction has varied from "why bother?" to "oh please
  dear god yes", revealing a (slightly surprising) range of reactions
  to the basic premise that while the data may be the same, analysis
  tools improve over time.  Because Harriet is a known member of the
  ocean biogeochem community (and hopefully because I am not viewed
  as evil by most people) I gather that people are cautiously optimistic
  about the effort.
  
Blog post: [MMETSP re-assemblies](https://monsterbashseq.wordpress.com/2016/09/13/mmetsp-re-assemblies/)
    
### Metagenome assembly analysis

We are close to a final draft of a paper on a project led by Sherine
Awad (postdoc, funded in part by Moore) to compare three metagenome
assemblers on a mock metagenome community.

Major highlights:

* all three assemblers more or less perform the same in terms of recovering
  content, but one assembler (MEGAHIT) is much, much faster and requires
  fewer resources.

* contamination in the mock metagenome turns out to be the cause of a
  mismatch between assembled content and expected content.

### Automated tools for transcriptomics

Camille Scott (graduate student) has developed two tools that are
critical in our scaling-up efforts, shmlast and dammit:

* https://github.com/camillescott/dammit

* https://github.com/camillescott/shmlast/
   
dammit is a transcriptome annotator pipeline that is already achieving
market dominance (because it actually works), while shmlast is a
(maintainable, Python) reimplementation of crb-blast that is used in
dammit for annotating transcripts.

### Continued development of khmer and screed

Our "flagship" software package, khmer, and its companion project,
screed, suffered from neglect for about a year after our 2.0 release
and the publication of our F1000 Research paper
([The khmer software package](https://f1000research.com/articles/4-900/v1)).
This was due in some part to the departure of Michael Crusoe, who was
our lead software engineer, and also in significant part to my
inability to lead the project scientifically at the same time as I was
trying to spin up the new lab at UC Davis.

In this past year, these issues were resolved by the arrival of Daniel
Standage (postdoc, funded entirely on an NIH R01), and the hiring of
Tim Head (software engineer/consultant).  Daniel is building a new
large-genome variant calling system on top of khmer called Kevlar, and
as a result is pushing khmer library development in new directions.
Tim is supporting the projects as open source projects, fixing bugs,
helping with code review, and generally doing the things that grad
students and postdocs find secondary to their research (but are
nonetheless important to software integrity, adaptibility, and forward
development).

khmer remains central to the lab and, a well as a suite of useful
exploratory tools, is now maturing into a robust platform that several
projects in the lab are relying on.  Despite this I am still somewhat
alarmed (at a strategic level) regarding the level of resources
required to achieve even a minimally responsible level of scientific
software development.

Major highlights:

* We finally have a sustainable way to move forward software
  development in the lab: have a postdoc or grad student take point
  scientifically, and support them with a (part time) PhD-level
  software engineer.  For our lab, a ratio of 1 half-time software
  engineer to 2-3 active grad/postdoc developers seems to work ok.
  
* Despite an increasing number of "eyes" on the code, and a frankly
  rather exhaustive (and exhausting) testing regime, we continue to
  find minor and not-so-minor bugs in khmer.  This suggests to me that
  plain ol' software bugs are likely to have a significant
  contribution to the repeatability/replication/reproducibility
  crisis.  (See Dave Soergel's paper, ["Rampant software errors may
  undermine scientific results"](https://f1000research.com/articles/3-303/v2.))
  
* Camille Scott (grad student) has made significant progress on streaming
  RNAseq assembly, which is laying the foundation for streaming analysis
  of very large continually arriving sequencing data sets.
  
* Our authorship policy for F1000 Research broke some people:
  [Pubwication of software papers, and authorship on them](http://ivory.idyll.org/blog/2015-authorship-on-software-papers.html)

### Development of MinHash-based technologies

The most significant shift in the lab focus over the last year
occurred with the publication of the mash paper from Adam Phillipy's
lab (Ondov et al., 2016).  The MinHash approach detailed in this paper
turns out to directly solve or provide a basis for solutions to a wide
range of critical problems, including metagenome comparison, indexing
sequence databases by content, and streaming classification of
sequencing data.

Major highlights:

* we developed our own toolkit, `sourmash`, for exploring MinHash
  sketches, and published v1.0 in the Journal of Open Source Software:
  [Sourmash in JOSS](https://github.com/openjournals/joss-reviews/issues/27)
      
* Luiz Irber (grad) implemented fast searches of very large databases
  of MinHash sketches using Sequence Bloom Trees (a technique first
  published by Carl Kingsford's lab).
  
* Luiz also implemented a distributed architecture for sketching very
  large sequence collections from Web-accessible archives
  (blog.luizirber.org/2016/12/28/soursigs-arch-1/).  This is connected to
  Casey Greene and Carl Kingsford's sequence refinery project.
  
* I used these tools to index all the microbial genomes and worked with Luiz
  to index and classify 400k public records from the NCBI Sequence Read
  Archive:
  
  * [Quickly searching all the microbial genomes](http://ivory.idyll.org/blog/2016-sourmash-sbt-more.html)
  * [Categorizing 400,000 microbial WGS samples](http://ivory.idyll.org/blog/2017-sourmash-sra-microbial-wgs.html)

* We initiated a collaboration with Blair Sullivan's group and Dominik
  Moritz Jeff Heer's lab at the DDD Barnraising at MDIBL to build
  tools combining contracted De Bruijn graphs, dominating sets, and
  MinHash-based search.  We hope this will lead to some major advances
  in metagenome and RNAseq analysis in the coming year.
