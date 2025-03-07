# psaca++

In my recent research, I have been investigating efficient implementations of
parallel suffix array construction algorithms (pSACA). Despite numerous
community-driven implementations emerging over the past decade, a comprehensive
benchmark and a production-ready implementation remain elusive.

To address this gap, this project aims to implement, collect and benchmark
existing pSACA implementations using a standardized dataset, providing a
unified interface for easy adoption and comparison.

> All the copyrights of implementations collected from the community are
> reserved by the original authors and the licenses are remained under licenses
> folder and the source files.

## Algorithms

* **Futamura-Aluru-Kurtz (2001)**: Futamura, Natsuhiko & Aluru, Srinivas & Kurtz, Stefan. (2001). Parallel Suffix Sorting.
* **pDC3 (2006)**: Kulla, Fabian & Sanders, Peter. (2007). Scalable Parallel Suffix Array Construction. Parallel Computing, Vol. 33(9).
* **parRange (2017)**: Labeit, Julian & Shun, Julian & Blelloch, Guy E. (2017). Parallel Lightweight Wavelet Tree, Suffix Array and FM-Index Construction. Journal of Discrete Algorithms, Vol. 43.
* **parDivSufSort (2017)**: Labeit, Julian & Shun, Julian & Blelloch, Guy E. (2017). Parallel Lightweight Wavelet Tree, Suffix Array and FM-Index Construction. Journal of Discrete Algorithms, Vol. 43.
* **pSAscan (2015)**: Kärkkäinen, Juha & Kempa, Dominik & Puglisi, Simon. (2015). Parallel External Memory Suffix Sorting.
* **PSAC (2015)**: Flick, P. & Aluru, S. (2015). Parallel Distributed Memory Construction of Suffix and Longest Common Prefix Arrays. In SC '15: Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis, Austin, TX, USA.
* **CaPS-SA (2024)**: Khan, J. & Rubel, T. & Molloy, E. et al. (2024). Fast, Parallel, and Cache-Friendly Suffix Array Construction. Algorithms Mol Biol, Vol. 19(16).
* **DCX (2024)**: Haag, Manuel & Kurpicz, Florian & Sanders, Peter & Schimek, Matthias. (2024). Fast and Lightweight Distributed Suffix Array Construction -- First Results. arXiv preprint arXiv:2412.10160. Available at: https://arxiv.org/abs/2412.10160.

## Related

For sequential SACA, [sacabench](https://github.com/sacabench/sacabench)
benchmarks 13 implementations from the community.
