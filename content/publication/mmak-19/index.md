---
title: "SURAA: A Novel Method and Tool for Loadbalanced and Coalesced SpMV Computations on GPUs"
date: 2019-01-01
publishDate: 2019-08-12T13:51:35.850947Z
authors: ["Thaha Muhammed", "Rashid Mehmood", "Aiiad Albeshri", "Iyad Katib"]
publication_types: ["2"]
abstract: "Sparse matrix-vector (SpMV) multiplication is a vital building block for numerous scientific and engineering applications. This paper proposes SURAA (translates to speed in arabic), a novel method for SpMV computations on graphics processing units (GPUs). The novelty lies in the way we group matrix rows into different segments, and adaptively schedule various segments to different types of kernels. The sparse matrix data structure is created by sorting the rows of the matrix on the basis of the nonzero elements per row (npr) and forming segments of equal size (containing approximately an equal number of nonzero elements per row) using the Freedman&ndash;Diaconis rule. The segments are assembled into three groups based on the mean npr of the segments. For each group, we use multiple kernels to execute the group segments on different streams. Hence, the number of threads to execute each segment is adaptively chosen. Dynamic Parallelism available in Nvidia GPUs is utilized to execute the group containing segments with the largest mean npr, providing improved load balancing and coalesced memory access, and hence more efficient SpMV computations on GPUs. Therefore, SURAA minimizes the adverse effects of the npr variance by uniformly distributing the load using equal sized segments. We implement the SURAA method as a tool and compare its performance with the de facto best commercial (cuSPARSE) and open source (CUSP, MAGMA) tools using widely used benchmarks comprising 26 high npr-variance matrices from 13 diverse domains. SURAA outperforms the other tools by delivering 13.99x speedup on average. We believe that our approach provides a fundamental shift in addressing SpMV related challenges on GPUs including coalesced memory access, thread divergence, and load balancing, and is set to open new avenues for further improving SpMV performance in the future."
featured: true
publication: "*Applied Sciences*"
#url_pdf: "https://www.mdpi.com/2076-3417/9/5/947"
doi: "10.3390/app9050947"
tags: ["SpMV", "HPC", "GPU", "iterative methods", "analysis", "sparse matrix storage", "load balancing", "coalesced access"]
projects: ["SpMV"]
---

