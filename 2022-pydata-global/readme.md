# Vaex: the perfect DataFrame Library for Python data apps

### Abstract

Vaex is an incredibly powerful DataFrame library that allows one to work with datasets much larger than RAM on a single node. It combines memory mapping, lazy evaluations, efficient C++ algorithms, and a variety of other tricks to empower your off-the-shelf laptop and make it crunch through a billion samples in real time.

A common use-case for Vaex is as a backend for data apps, especially if one needs to process, transform, and visualize a larger amount of data in real time. Vaex implements a number of features that have been specifically designed to improve performance of data hungry dashboards or apps, namely:
- caching
- async evaluations
- early stopping of operations
- progress bars

In this talk we will showcase how you can use these features to build efficient dashboards and data apps, regardless of the data app library you prefer using.


### Description

Working with datasets comprising millions or billions of samples is an increasingly common task, one that is typically tackled with distributed computing. Nodes in high-performance computing clusters have enough RAM to run intensive and well-tested data analysis workflows. More often than not, however, this is preceded by the scientific process of cleaning, filtering, grouping, and other transformations of the data, through continuous visualizations and correlation analysis. In today’s work environments, many data scientists prefer to do this on their laptops or workstations, as to more effectively use their time and not to rely on spotty internet connection to access their remote data and computation resources. Modern laptops have sufficiently fast I/O SSD storage, but upgrading RAM is expensive or impossible.

Applying the combined benefits of computational graphs, which are common in neural network libraries, with delayed (a.k.a lazy) evaluations to a DataFrame library enables efficient memory and CPU usage. Together with memory-mapped storage (Apache Arrow, HDF5) and out-of-core algorithms, we can process considerably larger data sets with fewer resources. As an added bonus, the computational graphs ‘remember’ all operations applied to a DataFrame, meaning that data processing pipelines can be generated automatically.

The computational efficiency of Vaex makes it a particularly good candidate for a backend of data hungry dashboards or data apps. In fact Vaex implements a variety of features that are specifically designed to help build efficient and memory-safe dashboards such as caching, async evaluations, fingerprinting, etc. With such features, one can build data intensive applications and even low-code tools while keeping the infrastructure cost and complexity lower. In this talk, we will present how one can take advantage of these special features of Vaex when building data applications.
