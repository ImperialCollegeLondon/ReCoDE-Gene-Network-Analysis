<!-- Your Project title, make it sound catchy! -->

# Project title

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
- Familiarity with Python
- Basic knowledge on NLP and LLMs
- Basic knowledge on single-cell RNA-sequencing
-->

### Academic

<!-- List the system requirements and how to obtain them, that can be as simple
as adding a hyperlink to as detailed as writting step-by-step instructions.
How detailed the instructions should be will vary on a case-by-case basis.

Here are some examples:

- 50 GB of disk space to hold Dataset X
- Anaconda
- Python 3.11 or newer
- Access to the HPC
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

To get started, first clone this repo, then change directories into it:
git clone https://github.com/AnjaliS1/ReCoDe-Gene-Network-Analysis.git
cd ReCoDe-Gene-Network-Analysis

If python virtualenv and Jupyter Lab isn't already installed on your system, install it using:
```python
  python3 -m pip install virtualenv
  python3 -m pip install jupyterlab
```
Then create a virtual environment for this exemplar:
```python
python3 -m venv venv_recode_GeneNetworkAnalysis
```
Source into your new virtual environment using:
```python
source venv_recode_firstdawn/bin/activate
```
Run this line to install all the necessary packages:
```python
pip install -r requirements.txt
```
Finally, run these two lines to setup your virtual env with jupyter lab notebook.
```python
pip install ipykernel
python -m ipykernel install --user --name=venv_recode_GeneNetworkAnalysis
```

-->

## Getting Started

<!-- An overview of the files and folder in the exemplar.
Not all files and directories need to be listed, just the important
sections of your project, like the learning material, the code, the tests, etc.

A good starting point is using the command `tree` in a terminal(Unix),
copying its output and then removing the unimportant parts.

You can use ellipsis (...) to suggest that there are more files or folders
in a tree node.

-->

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
