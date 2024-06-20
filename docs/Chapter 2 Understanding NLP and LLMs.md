# Chapter 2

## Introduction to NLP

Natural language processing (NLP) is an interdisciplinary subfield of computer science and information retrieval. Natural language such as text is processed using machine learning approaches with the goal for the computer to extract information as well as gain insights and context of the contained material.
There are two components to NLP, natural language generation (NLG) and natural language understanding (NLU). NLG consists of creating meaningful sentences from data, such as those seen in chatbots and voice assistants. NLU allows computers to understand and interpret texts instead. It can be used to analyse different aspect of language or map the input text into a different representation.

Common steps involved include:

- Sentence segmentation: Breaks down paragraphs into sentences.
- Word tokenisation: Breaks down sentences into separate words i.e. tokens.
- Stemming: Normalises words into root form i.e. recognises intelligence, intelligent and intellignetly, all come from the root “intelligen” (which is not a proper word).
- Lemmatisation: Similar to stemming but returns a proper word.
- Stop word analysis: Frequent non-important words, such as “a”, “is” etc are filtered out to focus on important words.
- Dependency parsing: To find relationships between words within a sentence through building a tree structure. A single word is assigned to be the parent node, and the main verb is assigned to be the root node.
- Part of speech tagging: Tags contain nouns, verbs, adverbs, adjectives that help to indicate meaning of words in a grammatically correct way in a sentence.

## Introduction on LLMs

A large language model (LLM) is a deep learning model that aims to predict and generate language. Transformers are a type of LLM, that use the self-attention mechanism.

Learning Outcomes:

- Be able to explain concepts of natural language processing.
- Understand what a large language model is and how it can be used for gene network analysis.
- Using the knowledge acquired, be able to use an already established model to create networks using python.

## scGPT

Mapping gene networks requires large amounts of transcriptomic data to learn relationships between genes, which is a hinderance in areas with limited data. With the advent and recent success of LLMs and generative pretrained models, they have now also been applied to the biological domain for gene network analysis. In particular, pretrained transformer models leverage advantages of deep learning, enabling predictions in cases with small datasets due to the context-aware, attention-based transformer architecture. Once pretrained on a large-scale dataset, they can calculate context specific predictions in settings with limited data. Furthermore, during the cell type annotation classification task, the network dynamics are captured in the weights of the model.

## Resources

For more information on NLP:

- <https://www.ibm.com/topics/natural-language-processing#:~:text=Natural%20language%20processing%2C%20or%20NLP,and%20generate%20text%20and%20speech>
- <https://www.turing.com/kb/natural-language-processing-function-in-ai>
