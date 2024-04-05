---
title: ""
draft: false
math: true
---

##### Software
---

github: [@jakryd](https://github.com/jakryd)  

* [PLUMED](https://www.plumed.org/) -- an open-source, community-developed library that provides methods for enhanced sampling, free energy estimation, and analysis of molecular dynamics (MD) simulations.

Modules for PLUMED2:
* [`lowlearner`](/software#lowlearner)
* [`maze`](/software#maze)

---------------------------------------------------------------------

##### `lowlearner`

---------------------------------------------------------------------

##### `maze`
---

`maze` (version 1.0) [[1,2]](#references)  
[Github](https://github.com/plumed/plumed2)

`maze` is a code that implements enhanced sampling methods for sampling the 
reaction pathways of ligand unbinding. It is made as a module for 
[PLUMED2](https://plumed.github.io/doc-v2.5/user-doc/html/index.html), an engine for 
free energy calculations of atomistic systems and enhanced sampling.

To use the module, you need enable `maze` by adding the `--enable-modules=maze` 
to the PLUMED configure command. You can follow the instructions given
[here](https://plumed.github.io/doc-v2.4/user-doc/html/_installation.html). 

For example:
```sh
> ./configure --enable-modules=maze
> make -j 4
> make install
```

You can ask questions or join the development discussion on
[PLUMED Google group](https://groups.google.com/forum/#!forum/plumed-users).

During its development, `maze` was funded by the National Science Center grants
no. 2015/19/N/ST3/02171, 2016/20/T/ST3/00488, and in part by 2016/23/B/ST4/01770.

1. __J. Rydzewski__  
  *maze: Heterogeneous Ligand Unbinding along Transient Protein Tunnels*  
  Comp. Phys. Commun. 247, 106865 (2020)  
  [DOI](https://doi.org/10.1016/j.cpc.2019.106865)
  [arXiv](https://arxiv.org/abs/1904.03929)
  [plumID:19.056](https://www.plumed-nest.org/eggs/19/056/)

2. __J. Rydzewski__, and O. Valsson  
  *Finding Multiple Reaction Pathways of Ligand Unbinding*  
  J. Chem. Phys. 150, 221101 (2019)  
  [DOI](https://doi.org/10.1063/1.5108638)
  [arXiv](https://arxiv.org/abs/1808.08089)
  [plumID:19.066](https://www.plumed-nest.org/eggs/19/066/)
