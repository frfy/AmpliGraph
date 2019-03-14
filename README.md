# AmpliGraph

**Open source Python library that predicts links between concepts in a knowledge graph.**

AmpliGraph is a suite of neural machine learning models for relational Learning, a branch of machine learning
that deals with supervised learning on knowledge graphs.


**Use AmpliGraph if you need to**:

* Discover new knowledge from an existing knowledge graph.
* Complete large knowledge graphs with missing statements.
* Generate stand-alone knowledge graph embeddings.
* Develop and evaluate a new relational model.


AmpliGraph's machine learning models generate **knowledge graph embeddings**, vector representations of concepts in a metric space:

![](docs/img/kg_lp_step1.png)

It then combines embeddings with model-specific scoring functions to predict unseen and novel links:

![](docs/img/kg_lp_step2.png)


## Key Features


* **Intuitive APIs**: AmpliGraph APIs are designed to reduce the code amount required to learn models that predict links in knowledge graphs.
* **GPU-Ready**: AmpliGraph is based on TensorFlow, and it is designed to run seamlessly on CPU and GPU devices - to speed-up training.
* **Extensible**: Roll your own knowledge graph embeddings model by extending AmpliGraph base estimators.


## Modules

AmpliGraph includes the following submodules:

* **KG Loaders**: Helper functions to load datasets (knowledge graphs).
* **Latent Feature Models**: knowledge graph embedding models. AmpliGraph contains: TransE, DistMult, ComplEx, ConvE, and RotatE.
* **Evaluation**: Metrics and evaluation protocols to assess the predictive power of the models.



## Installation

### Prerequisites

* Linux Box
* Python ≥ 3.6

##### Provision a Virtual Environment

Create and activate a virtual environment (conda)

```
conda create --name ampligraph python=3.6
source activate ampligraph
```

##### Install TensorFlow

AmpliGraph is built on TensorFlow 1.x.
Install from pip or conda:

**CPU-only**

```
pip install tensorflow==1.12.0

or

conda install tensorflow=1.12.0
```

**GPU support**

```
pip install tensorflow-gpu==1.12.0

or

conda install tensorflow-gpu=1.12.0
```



### Install AmpliGraph


Install the latest stable release from pip:

```
pip install ampligraph
```

If instead you want the most recent development version, you can clone the repository
and install from source (your local working copy will be on the latest commit on the `develop` branch).
The code snippet below will install the library in editable mode (`-e`):

```
git clone https://github.com/Accenture/AmpliGraph.git
cd AmpliGraph
pip install -e .
```


### Sanity Check

```python
>> import ampligraph
>> ampligraph.__version__
'1.0-dev'
```


## Predictive Power Evaluation (MRR Filtered)

|          |FB15k |WN18   |WN18RR |FB15K-237|
|----------|------|-------|-------|---------|
| TransE   | 0.55 | 0.50  | 0.23  | 0.32    |
| DistMult | 0.79 | 0.83  | 0.44  | 0.29    |
| ComplEx  | 0.79 | 0.94  | 0.44  | 0.30    |
| HolE     | 0.80 | 0.94  | 0.47  | 0.28    |


## Documentation

**[Documentation available here](http://docs.ampligraph.org)**

The project documentation can be built from your local working copy with:

```
cd docs
make clean autogen html
```

## How to contribute

See [guidelines](http://docs.ampligraph.org) from AmpliGraph documentation.


## How to Cite

If you like AmpliGraph and you use it in your project, why not starring the project on GitHub!

[![GitHub stars](https://img.shields.io/github/stars/accenture/ampligraph.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/accenture/ampligraph/stargazers/)


If you instead use AmpliGraph in an academic publication, cite as:

```
TODO
```

