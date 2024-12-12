---
title: ""
draft: false
math: true
---

##### Software
---

* [PLUMED](https://www.plumed.org/) -- an open-source, community-developed library that provides methods for enhanced sampling, free energy estimation, and analysis of molecular dynamics (MD) simulations.

Modules for PLUMED2:
* [`lowlearner`](/software#lowlearner)
* [`maze`](/software#maze)

---------------------------------------------------------------------

##### `lowlearner`

(version beta) [[1,2]](#references) / 
[zenodo](https://zenodo.org/records/4756093)   

`lowlearner` is a code for learning collective variables (CVs) from standard
and enhanced sampling simulations. Installation script and examples can 
be found in the Zenodo [dataset](https://zenodo.org/records/4756093). It is 
implemented as a module for  [PLUMED2](https://plumed.github.io/doc-v2.5/user-doc/html/index.html), 
an engine for free energy calculations of atomistic systems and enhanced 
sampling. The code requires PLUMED to be linked with LibTorch v1.8.

To use the module, you need enable `lowlearner` by adding the 
`--enable-modules=lowlearner` or `--enable-modules=all`
to the PLUMED configure command. You can follow the instructions given
[here](https://plumed.github.io/doc-v2.4/user-doc/html/_installation.html). 

For example:
```sh
> ./configure --enable-modules=lowlearner
> make -j 4
> make install
```

You can ask questions or join the development discussion on
[PLUMED Google group](https://groups.google.com/forum/#!forum/plumed-users).

---------------------------------------------------------------------

##### `maze`

(version 1.0) [[3,4]](#references) / [github](https://github.com/plumed/plumed2)  
(version 2.0) [[5]](#references) / [github](https://github.com/jakryd/plumed2-maze) / [tutorial](https://www.plumed-tutorials.org/lessons/24/008/data/)  

`maze` is a code that implements enhanced sampling methods for sampling the 
reaction pathways of ligand unbinding. It can be installed as a module in 
PLUMED similarly to the `lowlearner` module.

During its development, `maze` was funded by the National Science Center grants
no. 2015/19/N/ST3/02171, 2016/20/T/ST3/00488, and in part by 2016/23/B/ST4/01770.

###### References
1. __J. Rydzewski__, and [O. Valsson](https://www2.mpip-mainz.mpg.de/~valsson/)  
  *Multiscale Reweighted Stochastic Embedding: Deep Learning of Collective Variables for Enhanced Sampling*  
  J. Phys. Chem. A 125, 6286 (2021)  
  [doi:10.1021/acs.jpca.1c02869](https://doi.org/10.1021/acs.jpca.1c02869) /
  [arXiv:2007.06377](https://arxiv.org/abs/2007.06377) /
  [Zenodo:4756093](https://zenodo.org/record/4756093) /
  [plumID:21.023](https://www.plumed-nest.org/eggs/21/023/)

2. __J. Rydzewski__, M. Chen, T. K. Ghosh, [O. Valsson](https://www2.mpip-mainz.mpg.de/~valsson/)  
  *Reweighted Manifold Learning of Collective Variables from Enhanced Sampling Simulations*  
  J. Chem. Theory Comput. 18, 7179 (2022)  
  [doi:10.1021/acs.jctc.2c00873](https://doi.org/10.1021/acs.jctc.2c00873) /
  [arXiv:2207.14554](https://arxiv.org/abs/2207.14554) /
  [plumID:21.023](https://plumed-nest.org/eggs/21/023/)

3. __J. Rydzewski__  
  *maze: Heterogeneous Ligand Unbinding along Transient Protein Tunnels*  
  Comp. Phys. Commun. 247, 106865 (2020)  
  [doi:10.1016/j.cpc.2019.106865](https://doi.org/10.1016/j.cpc.2019.106865) /
  [arXiv:1904.03929](https://arxiv.org/abs/1904.03929) /
  [plumID:19.056](https://www.plumed-nest.org/eggs/19/056/)

4. __J. Rydzewski__, and [O. Valsson](https://www2.mpip-mainz.mpg.de/~valsson/)  
  *Finding Multiple Reaction Pathways of Ligand Unbinding*  
  J. Chem. Phys. 150, 221101 (2019)  
  [doi:10.1063/1.5108638](https://doi.org/10.1063/1.5108638) /
  [arXiv:1808.08089](https://arxiv.org/abs/1808.08089) /
  [plumID:19.066](https://www.plumed-nest.org/eggs/19/066/)


5. G.A. Tribello, M. Bonomi, G. Bussi, C. Camilloni, et al.  
  *PLUMED Tutorials: A Collaborative, Community-Driven Learning Ecosystem*    
  [arXiv:2412.03595](https://arxiv.org/abs/2412.03595)
