<!-- Your Project title, make it sound catchy! -->

# Single-Cell Gene Network Analysis using LLMs

<!-- Provide a short description to your project -->

## Description

The aim of this exemplar is to understand and demonstrate how to carry out single-cell gene network analysis on real data. Specifically, we will model networks in a small, publicly available Alzheimer's Disease dataset as well as explore them further through downstream analysis. This will consist of characterising the networks through gene set enrichment analysis and understanding the principles behind this. The modelling itself will encompass learning how to use deep learning techniques, such as natural language processing and large language models to construct networks. Together, this will provide an undertanding as well as practical experience with an end-to-end pipeline using single-cell data for gene network analysis.

<!-- What should the students going through your exemplar learn -->

## Learning Outcomes

- Gain an understanding be able to summarise the significance of biological networks in interpreting complex cellular processes and disease mechanisms.
- Be able to use knowledge of NLP and LLMs to apply a specific model to a test dataset, in order construct gene networks.
- Evaluate and relate findings to practical implications of gene networks in biological research through gene set enrichment analysis.

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

Structure this section as you see fit but try to be clear, concise and accurate
when writing your instructions.

For example:
Start by watching the introduction video,
then study Jupyter notebooks 1-3 in the `intro` folder
and attempt to complete exercise 1a and 1b.

Once done, start going through through the PDF in the `main` folder.
By the end of it you should be able to solve exercises 2 to 4.

A final exercise can be found in the `final` folder.

Solutions to the above can be found in `solutions`.
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
├── examples
│   ├── ex1
│   └── ex2
├── src
|   ├── file1.py
|   ├── file2.cpp
|   ├── ...
│   └── data
├── app
├── docs
├── main
└── test
```

<!-- Change this to your License. Make sure you have added the file on GitHub -->

## License

This project is licensed under the [BSD-3-Clause license](LICENSE.md)
