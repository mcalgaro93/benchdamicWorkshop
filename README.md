# An introduction to benchdamic

# Workshop description

This workshop provides an introductory example on how to work with the
analysis framework firstly proposed in **"Assessment of statistical
methods from single cell, bulk RNA-seq, and metagenomics applied to
microbiome data"** by [Calgaro et al.
(2020)](https://doi.org/10.1186/s13059-020-02104-1).

We will test a couple of methods for differential abundance (DA)
analysis on a microbiome dataset and we will see how to test custom
methods on the same dataset. Performances of each method are evaluated
with respect to i) suitability of distributional assumptions (GOF), ii)
ability to control false positives (TIEC), iii) concordance of the
findings, and iv) enrichment of DA microbial species in specific
conditions.

## Pre-requisites

-   Basic knowledge of R syntax
-   Familiarity with the `phyloseq` class
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

## Preparation

To be able to follow along with this workshop, we have created a
Docker installation. In order to access this, you need to
first install [Docker](https://docs.docker.com/engine/install/) on
your own computer. Once you have done that, you can then load the
Docker container for this workshop by starting Docker.

How you do this is dependent on your operating system.

### Windows

Hit the 'Windows' key (lower left on your keyboard, between Ctrl and
Alt), then type Docker. If Docker is installed you should see Docker
App highlighted - click Enter to start the App. It can take some time
to get started. You can see it's doing something by clicking on the
little caret (^) in the lower right of your screen - there should be a
little animated Docker icon which indicates it's starting. Once it is
started, open a CMD prompt by hitting the Windows key again and typing
cmd, then Enter. In the CMD prompt type

```
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 mcalgaro93/benchdamicWorkshop
```

You can choose any password for rstudio - that's what you will use to
log in. It will take some time for the Docker to be downloaded and
started, so you might consider doing this ahead of time.

### Linux

For Linux, it depends on how you installed. If you used a package
installer then presumably Docker will be set to start
automatically. Otherwise you need to start the Docker daemon by hand
(or set it to start automatically). There are too many variables to
give much detailed information here; for those on Linux, the
assumption is that you probably know what you are doing and can figure
it out from the Docker install page.

To start the daemon, if neccessary, do

```
sudo dockerd &
## followed by 
sudo docker run hello-world
```

If Docker is installed correctly it should print something
informative. To get the Docker container, it's the same as for
Windows.

```
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 mcalgaro93/benchdamicWorkshop
```

### MacOS

There is an installer for MacOS. As with Windows, follow the
instructions - it's just a regular drag'n'drop install. Once it's
installed and started, open a terminal prompt and as above type.

```
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 mcalgaro93/benchdamicWorkshop
```

## Run Docker

For all operating systems, once the Docker container is initialized,
you can access it by opening a browser and typing

```
http://localhost:8787
```

Which should present you with an RStudio login. Use rstudio as the
username and the password you used to start the Docker.


Then please open the file 'vignettes/introduction_to_benchdamic.Rmd' to start 
the workshop.
