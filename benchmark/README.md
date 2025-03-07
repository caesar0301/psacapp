# pSACABench

## Datasets

Candidates:

* 1000 Genomes Project, https://internationalgenome.org/
* CommonCrawl, https://commoncrawl.org/
* Wikipedia, https://dumps.wikimedia.org/

# Algorithms

### pDC3 (2006,2017)

* Sequential paper: Simple Linear Work Suffix Array Construction-03
* Parallel paper: Scalable Parallel Suﬃx Array Construction-06
* Parallel impl:
  * https://github.com/cmuparlay/pbbsbench/tree/master/benchmarks/suffixArray/parallelKS
  * https://github.com/aametwally/cloudSACA

### parRange (2007,2017)

* Sequential paper: N.J. Larsson, K. Sadakane, Faster suﬃx sorting, Theor. Comput. Sci. 387 (3) (2007) 258–272.
* Parallel paper: Parallel lightweight wavelet tree, suffix array and FM-index construction-17
* Paralle impl: https://github.com/cmuparlay/pbbsbench/tree/master/benchmarks/suffixArray/parallelRange

### parDivSufSort (2008,2017)

* Sequential papper: original none, supplementary Dismantling DivSufSort-17
* Parallel paper: Parallel lightweight wavelet tree, suffix array and FM-index construction-17
* Parallel impl (shared memory): use similar method like parallel range + libdivsufsort
* Integrated into SDSL: https://github.com/simongog/sdsl-lite/compare/master...jlabeit:sdsl-lite:parallel_sdsl
* Comparison: parDivSufSort > pDC3 > parRange. And parDivSufSort outperforms in most cases. pDC3 outperforms in some cases.

### Parallel Futamura-Aluru-Kurtz (2001,2015)

Distributed implementation of Futamura-Aluru-Kurtz (2001) and pDC3 (2006).

* Sequential papper: Parallel suffix sorting (FAK)
* Parallel paper: Cloud-based parallel suffix array construction based on MPI, Distributed suffix array construction algorithms: Comparison of two algorithms
* Parallel Impl: https://github.com/aametwally/cloudSACA
* Comparison: FAK > pDC3

### pSAscan (2015)

* Parallel paper: Parallel External Memory Suﬃx Sorting
* Parallel impl: https://www.cs.helsinki.fi/group/pads/pSAscan.html
* Comparison: pSAscan (internal memory) > pDC3, pSAscan (external memory) > eSAIS

### Flick-Aluru Algorithm (2015)

* Parallel paper: Parallel Distributed Memory Construction of Suffix and Longest Common Prefix Arrays
* Parallel impl: https://github.com/patflick/psac
* Comparison: FA2015 > FAK (cloudSACA)

### CaPS-SA (2024)

* Parallel paper: Fast, parallel, and cache‑friendly suffix array construction
* Parallel impl: https://github.com/jamshed/CaPS-SA
* Comparison: CaPS-SA > pDC3 > parDivSufSort (conflicted result)

## Benchmarking

SOTA: FAS2015, pSAscan

TODO: FA2015, FAK (cloudSACA), pSAscan, parDss, pDC3

## Related

### EM-SparsePhi (construct LCP from SA)

* Paper: Better external memory LCP array construction
* impl: https://www.cs.helsinki.fi/group/pads/better_em_laca.html

### LCPscan

* paper: LCP Array Construction in External Memory
* impl: https://www.cs.helsinki.fi/group/pads/LCPscan.html
