gappa is a collection of commands for working with phylogenetic data.
A typical use case is the evolutionary placement of short environmental (metagenomic) sequences on a reference phylogenetic tree.
<!-- See [Phylogenetic Placement](../wiki/Phylogenetic-Placement) for an introduction describing a typical pipeline. -->
<!-- It however also offers some commands for working with data such as sequences or trees. -->

Many commands in gappa are implementations of our novel methods.
At the same time, it offers some commands that are also implemented in the excellent
[guppy](http://matsen.github.io/pplacer/generated_rst/guppy.html) tool.
However, being written in C++, gappa is much faster and needs less memory for most of the tasks.

## Phylogenetic Placement

We recommend our review article as an introduction to the topic of phylogenetic placement:

> Metagenomic Analysis Using Phylogenetic Placement — A Review of the First Decade.<br />
> Lucas Czech, Alexandros Stamatakis, Micah Dunthorn, and Pierre Barbera.<br />
> Frontiers in Bioinformatics, 2022. https://doi.org/10.3389/fbinf.2022.871393<br />

<!-- The typical phylogenetic placement pipeline looks like this:
![Phylogenetic Placement Pipeline.](https://github.com/lczech/gappa/blob/master/doc/png/pipeline.png?raw=true)
-->

<!-- The most common programs for conducting this analysis are [EPA-ng](https://github.com/Pbdas/epa-ng),
[RAxML-EPA](http://sco.h-its.org/exelixis/web/software/epa/index.html) and
[pplacer](http://matsen.fhcrc.org/pplacer/). They usually store the data in
[jplace](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0031009) files, which is what many gappa commands work with. -->

For a full stack example of conducting phylogenetic placement with EPA-ng, [see here](https://github.com/Pbdas/epa-ng/wiki/Full-Stack-Example).

## Command Line Interface

gappa is used via its command line interface, with subcommands for each task.
The commands have the general structure:

    gappa <module> <subcommand> <options>

The modules are simply a way of organizing the commands.

## Modules

 * Module `analyze`: Analyze and compare different `jplace` files, that is, find differences and patterns between different samples.
 * Module `edit`: Edit, manipulate, and transform files in different formats.
 * Module `examine`: Examine, visualize, and tabulate information in files.
 * Module `prepare`: Prepare and generate data and files needed to run typical pipelines and analyses.
 * Module `simulate`: Simple random generation of files for testing.
