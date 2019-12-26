---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Novel Techniques for Large Sparse Linear Equation Systems"
summary: "Adaptive techniques for sparse storage and multiplication"
authors: ["Thaha Mohammed", "Rashid Mehmood"]
tags: ["HPC", "SpMV"]
categories: []
date: 2019-08-14T12:17:56+03:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Some caption that goes well"
  focal_point: "Smart"
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Sparse Matrix-Vector multiplication (SpMV) is one of the key operations in linear algebra that lies at the heart of diverse domains such as scientific computing, engineering, economic modeling, and information retrieval, to name a few. They play a significant role in solving linear system of equations using iterative methods. Sparse Kernels are computational operations on matrices whose entries are mostly zero so that computations with and storage of these zero elements may be eliminated. The emergence of parallel architectures, especially GPU, while offering higher computational performance, has led to the redesign of existing algorithms to suit the architecture. Specialized storage structures are used to improve the performance of sparse SpMV. These structures have design issues for translating it to GPUs. Special SpMV must be designed using these structures to improve the performance on GPUs.

Implementation of parallel iterative solvers on GPU has numerous issues. Specialized storage structures are used to improve the performance of sparse SpMV. These structures have design issues for translating it to GPUs. The problems faced in implementing parallel sparse iterative solvers and converting sparse structures to GPU is as listed below:

1. Coalesced memory access to both the sparse matrix A and the vector y
2. Load balance among array threads and warps
3. Thread divergence among a warp of threads.
4. Performance variance based on the structure of the sparse matrices
5. The amount of memory access required for computations.

Depending upon the sparsity of the structure the performance of the matrices vary and issues such as coalesced memory access, load balancing among threads, and thread divergence are dependent upon the sparsity structure of the matrices. The sparse storage schemes that satisfy the above conditions does not necessarily satisfy these conditions for other matrices and hence there is a performance deterioration. The sparsity structure of the sparse matrices varies from matrix to matrix, and application domain to domain. The performance of the SpMV kernel is dependent upon the sparsity structure of the matrices. We can deduce that none of the sparse
representation schemes are perpetually superior rather the SpMV performance depends upon the sparse representation and the choice of sparse representation is based on the sparsity structure. The GPU architecture used for SpMV computations and the thread-block-warp configuration of the SpMV kernel are two other factors that affect the performance of SpMV kernel on GPUs.

In this research, we propose a new adaptive schemes and techniques that dynamically uses the best possible storage format that gives the maximum performance depending upon the sparsity structure of the matrices. The idea is to have sparse storage scheme that dynamically satisfies load balancing, and coalesced memory access without thread divergence.
