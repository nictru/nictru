# Hey, nice to meet you!

I am an aspiring bioinformatician and computational biologist. My primary fields of interests are pipeline development and machine learning in bulk, single-cell and non-coding transcriptomics.

Currently, I am doing an internship at [Orakl Oncology](https://www.orakl-oncology.com/), where I am working on the integration of multi-modal organoid datasets.

Below, you can find an overview of my most relevant work.
If you find it useful or want to connect, feel free to follow me on LinkedIn and GitHub, or reach out via E-Mail.

## Past and ongoing projects

### Bachelor's thesis: Circular RNAs in Estrogen Signaling and Breast Cancer Biology

This project was based on data from mouse models. A major part of it was the robust detection of circRNAs and identifying potential regulatory roles. Identified many molecules that are already known, but also some novel hits. Details can be found in the [dedicated repository](https://github.com/nictru/bsc-thesis). The pipeline for detecting and quantifying circRNAs is now available as [`nf-core/circrna`](https://nf-co.re/circrna).

### Single cell atlas construction: COST MyeInfoBank

[COST MyeInfoBank](https://www.mye-infobank.eu/home.html) is a consortium of biologists and bioinformaticians that aims on deepening the understanding of myeloid cells inflammatory diseases and cancer. The working group I am involved with focuses on the construction of single-cell transcriptomic atlases of relevant diseases, and drawing insights about myeloid cells from these atlases.

For this purpose, I built a pipeline that allows building such atlases in a scalable and reproducible way. While originally called SIMBA, the pipeline is now available as [`nf-core/scdownstream`](https://nf-co.re/scdownstream). More information about my role in the consortium can be found in [this article](https://www.mye-infobank.eu/news/newsreader-2/YR7.html).

### VASA-Seq data analysis

This was a university project at the [Battich lab](https://www.battichlab.org/). VASA-Seq is a relatively new protocol for single cell transcriptomics, that allows capturing non-coding transcripts. Since there is no established workflow for processing this data yet, I developed a version of [`nf-core/scrnaseq`](https://nf-co.re/scrnaseq) that is tailored for VASA-Seq data. The resulting pipeline can be found [here](https://github.com/nictru/vasaseq).

Key differences to the mainstream [`nf-core/scrnaseq`](https://nf-co.re/scrnaseq) are:

- Genome preprocessing (include custom FASTA snippets for transcripts that are not annotated in the reference genome, like rRNA)
- Allow obtaining spliced and unspliced counts for RNA velocity analysis using STARsolo (this has since been merged into `nf-core/scrnaseq`)

## Pipeline development

I am the primary maintainer of three nf-core pipelines:

- [`nf-core/scdownstream`](https://nf-co.re/scdownstream): Takes count matrices as input and performs QC, integration, clustering and some follow-up tasks. Originally implemented for the creation of single-cell atlases in the COST MyeInfoBank consortium.
- [`nf-core/circrna`](https://nf-co.re/circrna): Allows to detect and quantify circular RNAs, investigate miRNA interactions and to perform statistical tests. I implemented this as part of my Bachelor's thesis.
- [`nf-core/tfactivity`](https://nf-co.re/tfactivity): Takes donor-matched bulk transcriptomics and open chromatin data (e.g. ATAC-Seq, Histone ChIP-Seq) from two or more conditions as input. Tries to identify transcription factors that are differentially active across the provided conditions.

Also I am assisting the development of two more nf-core pipelines:

- [`nf-core/scrnaseq`](https://nf-co.re/scrnaseq): Takes FastQ files from droplet-based scRNA-Seq technologies as input, performs read-level QC, alignment and quantification, provides the user with count matrices.
- [`nf-core/hadge`](https://github.com/theislab/hadge): This one is not in nf-core yet, but will be soon. It allows processing of genotype-multiplexed scRNA-Seq datasets. Output are count matrices, just like in `nf-core/scrnaseq`.


