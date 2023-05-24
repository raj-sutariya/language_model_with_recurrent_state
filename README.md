# Scalability Analysis of Language Models with Recurrent State Computation

This repository contains the code and documentation for a project aimed at analyzing the scalability of language models with recurrent state computation. 

## Stages of the Project

The project can be divided into the following stages:

1. **Literature review of alternatives to self-attention for large language models.** The focus of this stage is on methods with stateful inference, i.e. where the next step only depends on the previous step (O(1)) instead of the entire sequence (O(L)). Candiate models are transformers with linear attention and linear recurrent units.

2. **Development of a software toolkit for training, profiling, and comparing LLM.** This stage involves creating a toolkit to facilitate the training, profiling, and comparison of various language models. This will include scripts for preprocessing datasets, training models, and testing their performance.

3. **Benchmark against transformers along various dimensions.** In this stage, multiple benchmarks will be performed against transformer models along different dimensions, including:
- Different parameter sizes (ranging from 50M to 1B)
- Different numbers of training data (tokens) sizes, with optimal numbers determined according to recent literature
- Different context lengths

4. **Compare models in terms of inference latency and estimated energy consumption.** Using FLOPs and memory access as metrics, the models will be compared in terms of their inference latency and estimated energy consumption.

5. **Discuss suitability for neuromorphic implementations.** In the final stage, the suitability of the different models for neuromorphic implementations will be discussed. 

### Literature Review

The literature review section provides an overview of the methods that use stateful inference, i.e., where the next step only depends on the previous step instead of the entire sequence. This approach has a time complexity of O(1) compared to the traditional approach with a time complexity of O(L), where L is the length of the input sequence. The review investigates the following candidate models:

* Transformers with Linear Attention
* Linear Recurrent Units

### Development of a Software Toolkit

The project also includes the development of a software toolkit that streamlines the training, profiling, and comparison of large language models. The toolkit aims to simplify the process of benchmarking language models against each other.

### Benchmarking

The benchmarking section evaluates the scalability of different models along the following dimensions:

* Parameter sizes ranging from 50M to 1B
* Number of training data (tokens) sizes, computed according to recent literature for optimal performance
* Different context lengths

The language models are compared in terms of their inference latency and estimated energy consumption by measuring the required FLOPs (floating-point operations) and memory access.

### Suitability for Neuromorphic Implementations

Finally, the project analyzes the suitability of the models for neuromorphic implementations. Neuromorphic computing refers to the use of hardware that mimics the structure and functionality of biological neural networks. The discussion focuses on how the models can be optimized for such hardware.

Overall, this repository offers a comprehensive analysis of the scalability of language models using recurrent state computation, comparing various models and discussing their potential for neuromorphic implementations.

## Getting Started

To use the code in this repository, you will need to have Python 3.7 or higher installed on your system. You will also need to install the required dependencies, which can be done using pip. 

Please see the [documentation](./docs/index.md) for more detailed instructions on how to get started, as well as information on how to use the toolkit and perform the benchmarks. 
