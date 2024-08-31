# NER-Tutorial-SS2024

## 1. About
This repository constains the code and data for a Multiclass classification task to determine whether a given word is a Named Entity and identify its type.

**A short summary of the Tutorial:**

This tutorial aims to present a real computational linguistics problem: solving a multiclass classification task to determine whether a given word is a Named Entity and identify its type. 

The input consists of sentences extracted from the "Corpus for Named Entity Recognition" using the Groningen Meaning Bank corpus (University of Groningen, 2020). This corpus includes thousands of texts in both raw and tokenized formats, along with annotations for parts of speech, named entities, lexical categories, and other natural language structural phenomena. (more at [Groningen Meaning Bank](https://developer.ibm.com/exchanges/data/all/groningen-meaning-bank/)).

The dataset with 1M x 4 dimensions contains columns "Sentence, Word, POS, Tag", it is grouped by Sentence and available in [Kaggle](https://www.kaggle.com/datasets/namanj27/ner-dataset) (one token per line).

There are 17 labels for NER: **B-per, I-per, B-gpe, I-gpe, B-tim, I-tim, B-eve, I-eve, B-art, I-art, B-nat, I-nat, B-org, I-org, B-geo, I-geo and O (Outside tags)**.

> (**B** stands for *"Beginning"* and **I** stands for *"Inside"*.)
>
>### Examples:
>
>For **"Elton John"**:  
>- **B-per** = Elton  
>- **I-per** = John
>
>For **"Sir Elton John"**:  
>- **B-per** = Sir  
>- **I-per** = Elton  
>- **I-per** = John

They represent 8 standard named entity recognition tags as follows:

| **Abbreviation** | **Meaning**               |
|------------------|---------------------------|
| **per**          | Person                    |
| **gpe**          | Geopolitical Entity       |
| **tim**          | Time indicator            |
| **eve**          | Event                     |
| **art**          | Artifact                  |
| **nat**          | Natural Phenomenon        |
| **org**          | Organization              |
| **geo**          | Geographical Entity       |

## 2. Steps Overview

The two steps we will perform are the following:

1. **Pre-processing data.**
2. **Create a multi-class classifier with Neuron Networks using Keras.**

