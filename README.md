## Overview

This is an Approximation algorithm for the Euclidean Minimum Spanning Tree (EMST) problem. It offers the following features:

- **For High-Dimensional and Million-Scale Datasets**: This algorithm is specifically designed for high-dimensional data and has been tested on real-world datasets with millions of data points.
- **High-Quality Results**: It provides a high-precision approximation of the EMST length and generates a structure similar to the exact result.
- **Parallelizable**: The computational workload, which is the most intensive part of the algorithm, is implemented using FAISS and is parallelizable.

## Prerequisites (Required Libraries)

The following libraries need to be installed for this project to run. (These are the versions used during the experiments.)

- **faiss-cpu**: version 1.8.0
- **Eigen**: version 3.4.0
  
## Installation

To install and run the project locally, follow these steps:

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/KAKu99/approx_emst_2024.git
    ```

2. Navigate to the project directory:
    ```bash
    cd approx_emst_2024
    ```

3. Build the project:
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ```

## Usage

The data folder structure should be as follows. Each dataset must be prepared beforehand.

```bash
  ─── data/ # Directory for input datasets. Please input this path to exp.sh. 
   ├── fasttext/
   │ └── wiki-news-300d-1M.vec
   ├── glove/
   │ └── twitter/
   │  └── wiki-news-300d-1M.vec
   ├── mnist/
   │ └── train-images-idx3-ubyte
   └── sift/
     └── sift_base.fvecs
```

Here's an example command. You can adjust the settings in 'exp.sh'.

```bash
# Example command to run the project
bash exp.sh your/data/folder/path
```
