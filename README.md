# An introduction to benchdamic

# Workshop description

This workshop provides an introductory example on how to work with the
analysis framework firstly proposed in **"Assessment of statistical
methods from single cell, bulk RNA-seq, and metagenomics applied to
microbiome data"** by [Calgaro et al.
(2020)](https://doi.org/10.1186/s13059-020-02104-1) and then formalised
in the `benchdamic` Bioconductor package [Calgaro et al.
(2023)](https://doi.org/10.1093/bioinformatics/btac778).

We will test a couple of methods for differential abundance (DA)
analysis on a microbiome dataset and we will see how to test custom
methods on the same dataset. Performances of each method are evaluated
with respect to i) suitability of distributional assumptions (GOF), ii)
ability to control false positives (TIEC), iii) concordance of the
findings, and iv) enrichment of DA microbial species in specific
conditions.

## Pre-requisites

-   Intermediate knowledge of R syntax
-   Familiarity with the `phyloseq` or `TreeSummarizedExperiment`
    classes
-   Familiarity with DA analysis in microbiome data

Some suggested background readings for the workshop:

-   "Assessment of statistical methods from single cell, bulk RNA-seq,
    and metagenomics applied to microbiome data" by [Calgaro et al.
    (2020)](https://doi.org/10.1186/s13059-020-02104-1)
-   "Microbiome differential abundance methods produce different results
    across 38 datasets" by [Nearing et al.
    (2022)](https://doi.org/10.1038/s41467-022-28034-z);
-   "Normalization and microbial differential abundance strategies
    depend upon data characteristics" by [Weiss et al.
    (2017)](https://doi.org/10.1186/s40168-017-0237-y);
-   "benchdamic: benchmarking of differential abundance methods for
    microbiome data" by [Calgaro et al.
    (2023)](https://doi.org/10.1093/bioinformatics/btac778).

## Preparation

To be able to follow along with this workshop, we have created a Docker
installation. In order to access this, you need to first install
[Docker](https://docs.docker.com/engine/install/) on your own computer.
Once you have done that, you can then load the Docker container for this
workshop by starting Docker and writing the following line in your
terminal:

```         
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 ghcr.io/mcalgaro93/benchdamicworkshop
```

You can choose any password for rstudio - that's what you will use to
log in. It will take some time for the Docker to be downloaded and
started, so you might consider doing this ahead of time.

In linux, you may experience an error: "docker: Got permission denied
while trying to connect to the Docker daemon socket...". To solve it
just run the command with `sudo` privilegies or follow this
[thread](https://stackoverflow.com/questions/48957195/).

Once running, navigate to <http://localhost:8787/> and then login with
'rstudio' as username and the chosen password as password.

Then please open the file 'vignettes/introduction_to_benchdamic.Rmd' to
start the workshop.

You can also see the workshop material at
<https://mcalgaro93.github.io/benchdamicWorkshop/>.
