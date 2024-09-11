<!-- Your Project title, make it sound catchy! -->

# Single-Cell Gene Network Analysis

<!-- Provide a short description to your project -->

## Description

The aim of this exemplar is to understand and demonstrate how to carry out single-cell gene network analysis on real data. Specifically, we will model networks in a small, publicly available Human Cancer dataset as well as explore them further through downstream analysis. This will consist of characterising the networks through gene set enrichment analysis and understanding the principles behind this. The modelling itself will encompass learning how to use both correlation-based approaches as well as deep learning techniques, such as large language models to construct networks. Together, this will provide an undertanding as well as practical experience with an end-to-end pipeline using single-cell data for gene network analysis.

<!-- What should the students going through your exemplar learn -->

## Overall Learning Outcomes

By the end of the series of chapters and notebooks you should be able to:

1. Understand the Foundations of Single-Cell RNA-Sequencing (scRNA-seq):
  - Comprehend the steps involved in scRNA-seq data processing, including generating count     matrices and performing quality control.
  - Explain how scRNA-seq differs from bulk RNA-seq in capturing cellular heterogeneity.
  - Explore publicly available snRNA-seq data and process it for downstream analysis using Python.
2. Apply Techniques in Gene Network Analysis:
  - Understand the concepts and methods involved in constructing gene networks from scRNA-seq data.
  - Identify relationships between genes using co-expression based approaches.
  - Visualise gene networks using tools such as NetworkX.
3. Carry Out Gene Set Enrichment Analysis:
  - Explain the significance of gene set enrichment and its role in interpreting gene networks.
  - Perform pathway-based enrichment analyses using curated gene sets from resources like KEGG and Gene Ontology (GO).
  - Apply statistical tests such as the Fisher Exact Test to assess the overrepresentation of gene sets.
  - Implement multiple hypothesis correction methods like the false discovery rate (FDR) to ensure robust enrichment results.
4. Utilise Large Language Models for Gene Network Predictions:
  - Explain the basic principles of NLP, including tokenization, stemming, and dependency parsing.
  - Recognize the capabilities of LLMs in analyzing complex biological datasets, even when data is limited.
  - Apply pretrained models like scGPT to predict gene interactions and network dynamics in scRNA-seq data.
  - Understand the role of transformers and attention mechanisms in enhancing biological predictions through context-aware learning.

<!-- How long should they spend reading and practising using your Code.
Provide your best estimate -->

| Task       | Time    |
| ---------- | ------- |
| Reading    | 3 hours |
| Practising | 3 hours |

## Requirements

<!--
-->
- Familiarity with Python
- Basic knowledge on NLP and LLMs
- Basic knowledge on single-cell RNA-sequencing

## Getting Started

Take a look at the table of contents below and follow the chapters from 1 to 4. These are also aligned with the notebooks and should give you background information as well as direction and motivation behind the notebooks. If you are ever unsure or don't understand how to do something on the workbooks, there are also fully worked through solutions that you can use.

### Cloning the repository

If you don't have it already, install git to your machine, see [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for details on all OS's.

Once installed, run the following to clone the repository and change the working directory to the clones repository:

```bash
git clone https://github.com/ImperialCollegeLondon/ReCoDE-Gene-Network-Analysis.git
cd ReCoDE-Gene-Network-Analysis
```

### Setting up your environment

Before installing the project dependencies, it's recommended to set up a virtual environment. This ensures that the dependencies for this project do not interfere with those of other Python projects you may be working on. Follow these steps to create and activate a virtual environment:

1. **Create a Virtual Environment**

If you haven't already, navigate to the root directory of the project and run the following command to create a virtual environment. This command creates a new directory `.venv` which will contain all the necessary executables to use the packages that a Python project would need.

  ```bash
  python3 -m venv .venv
  ```

1. **Activate the Virtual Environment**

After creating the virtual environment, you need to activate it. Activation of the virtual environment will change your shell’s prompt to show what virtual environment you’re using, and modify the environment so that running python will get you that particular version and installation of Python.
  
- **On Windows**

```bash
.\venv\Scripts\activate
```

- **On Unix or MacOS**

```bash
source venv_recode_GeneNetworkAnalysis/bin/activate
```

This command needs to be run every time you start a new terminal session and want to work on this project.

1. **Install Dependencies**

With the virtual environment activated, install the project dependencies by running:

```bash
pip install -r requirements.txt
```

Remember to deactivate your virtual environment when you're done working on the project by running deactivate.

<!-- An overview of the files and folder in the exemplar.
Not all files and directories need to be listed, just the important
sections of your project, like the learning material, the code, the tests, etc.

A good starting point is using the command `tree` in a terminal(Unix),
copying its output and then removing the unimportant parts.

You can use ellipsis (...) to suggest that there are more files or folders
in a tree node.

-->

### System

<!-- Instructions on how the student should start going through the exemplar.

Each jupyter notebook workbook is paired with a chapter of information ordered from 1 to 4. The notebooks can be accessed within the notebooks folder and the chapters can be accessed within the docs folder. Upon completion, you can go through the solutions notebooks which are also stored in the docs folder. 

-->

## Development

This project uses `pre-commit` and `pip-tools` for managing pre-commit hooks and dependencies respectively. Follow these steps to set up your development environment:

### Setting up pre-commit

1. Install pre-commit on your system. If you haven't installed it yet, you can do so by running:

```sh
pip install pre-commit
```

1. Once installed, you can set up the pre-commit hooks by running the following command in the root directory of this project:

```sh
pre-commit install
```

This will install all the pre-commit hooks defined in .pre-commit-config.yaml into your local repository. These hooks will automatically run on every commit to ensure code quality and consistency.

### Managing Dependencies with pip-tools

Dependencies are managed using the [pip-tools](https://github.com/jazzband/pip-tools) tool chain.

Unpinned dependencies are specified in `pyproject.toml`. Pinned versions are then produced with:

```bash
pip-compile pyproject.toml
```

To add/remove packages edit `pyproject.toml` and run the above command. To upgrade all existing dependencies run:

```bash
pip-compile --upgrade pyproject.toml
```

Dependencies for developers are listed separately as optional, with the pinned versions being saved to `dev-requirements.txt` instead.

`pip-tools` can also manage these dependencies by adding extra arguments, e.g.:

```bash
pip-compile -o dev-requirements.txt --extra=dev pyproject.toml
```

When dependencies are upgraded, both requirements.txt and dev-requirements.txt should be regenerated so that they are in sync.

## Project Structure

```log
.
├── .github/workflows
├── data
|   ├── data
|       ├── Bcell_datExpr_pseudobulk.csv
│       └── Bcell_filtered_compressed.h5ad.gz
|   ├── metadata
|       ├── Bcell_metadata.csv
│       └── Bcell_metadata_pseudobulk.csv
│   └── other
|       ├── h.all.v2023.2.Hs.symbols.gmt
│       └── separated_communities.pkl
├── docs
|   ├── .icons/logos
|   ├── assets
|   ├── Chapter 1: Background on Single-Cell RNA-Sequencing
|   ├── Chapter 2: Gene Network Analysis
|   ├── Chapter 3: Gene Network Downstream Analysis
│   └── Chapter 4: Understanding NLP and LLMs
├── notebooks
|   ├── solutions
|       ├── 1.Correlation_Network_Analysis_and_Visualisation_Solution.ipynb
|       ├── 2.Network_Analysis_Solution.ipynb
|       ├── 3.Fisher_Exact_Test_Solution.ipynb
│       └── 4.SCGPT_Solution.ipynb
|   ├── workbooks
|       ├── 1.Correlation_Network_Analysis_and_Visualisation_Workbook.ipynb
|       ├── 2.Network_Analysis_Workbook.ipynb
|       ├── 3.Fisher_Exact_Test_Workbook.ipynb
│       └── 4.SCGPT_Workbook.ipynb
|   ├── .placeholder
|   ├── process_data.ipynb
├── test
|   ├── test_placeholder.py
├── .gitignore
├── .pre-commit-config.yaml
├── LICENSE.md # Outlines what legal rights you have to use this software.
├── README.md  # You are here!
├── dev-requirements.txt # Development requirements
├── mkdocs.yml # Tells readthedocs.com how to build the documentation.
├── pyproject.toml # Machine readable information about the package.
├── requirements.txt # Requirements for the notebooks.
└── test
```

## License

This project is licensed under the [BSD-3-Clause license](LICENSE.md)
