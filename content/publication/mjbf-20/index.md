---
title: "Distributed Inference Acceleration with Adaptive DNN Partitioning and
Offloading"
date: 2020-04-27
publishDate: 2020-01-17T13:51:35.852572Z
authors: ["Thaha Mohammed", "Carlee Joe-Wong","Rohit Babbar", Mario Di
Francesco"]
publication_types: ["2"]
abstract: "Deep neural networks (DNN) are the de-facto solution behind many intelligent applications of today, ranging from machine translation to autonomous driving. DNNs are accurate but resource-intensive, especially for embedded devices such as smartphones and smart objects in the Internet
of Things. To overcome the related resource constraints, DNN inference is
generally offloaded to the edge or to the cloud. This is accomplished by
partitioning the DNN and distributing computations at the two different
ends. However, existing solutions simply split the DNN into two parts, one
running locally or at the edge, and the other one in the cloud. In
contrast, this article proposes a solution to divide a DNN in multiple
partitions that can be processed locally by end devices or offloaded to one
or multiple powerful nodes, such as in fog networks. The proposed solution
includes both an adaptive DNN partitioning scheme and a distributed
algorithm to offload computations based on a matching game approach.
Results obtained by using a self-driving car dataset and several DNN
benchmarks show that the proposed solution significantly reduces the total
latency for DNN inference compared to other distributed approaches and is
2.6 to 4.2 times faster than the state of the art."
featured: false
publication: "*IEEE INFOCOM 2020 - IEEE Conference on Computer Communications (INFOCOM
2020)*"
#url_pdf: "https://doi.org/10.1007/978-3-030-13705-2_17"
doi: "None"
tags: ["DNN inference", "Task partitioning", "Task offloading","Distributed algorithm"]
projects: ["Fog"]
---