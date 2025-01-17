# Implementing Latent Dirichlet Allocation (LDA) in Python

This project demonstrates the implementation of Latent Dirichlet Allocation (LDA) for topic modeling using Python. It covers data preprocessing, topic extraction, and visualization of topics.

## Key Features
- **Data Preprocessing**: Tokenization, removal of stopwords, and preparation of data for LDA.
- **Topic Modeling**: Utilizing Gensim's LDA model to identify hidden topics in text data.
- **Visualization**: Interactive visualization of topics using pyLDAvis.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Setup and Installation](#setup-and-installation)
3. [Usage](#usage)
4. [Key Code Highlights](#key-code-highlights)
5. [Dependencies](#dependencies)
6. [License](#license)

---

## Introduction

Latent Dirichlet Allocation (LDA) is a popular topic modeling algorithm used for discovering hidden topics in a collection of documents. This implementation allows users to extract and visualize topics from a corpus of text files.

---

## Setup and Installation

### Prerequisites
- Python 3.7 or higher
- A working knowledge of Python and basic natural language processing concepts.

### Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/abderazzakelmernissi/GenAI_SR_LDA_Code.git
    cd lda-topic-modeling
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Usage

1. **Prepare the Dataset**: Place all `.txt` files in a folder. Update the folder path in the `load_data()` function in the script.

2. **Run the Script**:
    Execute the main Python script to preprocess the data and perform LDA:
    ```bash
    python lda_model.py
    ```

3. **Visualize Topics**:
    After running the script, an interactive HTML visualization of the topics will be generated using pyLDAvis.

---

## Key Code Highlights

### Loading the Dataset
The `load_data` function reads all `.txt` files from a specified folder and combines them for preprocessing.

```python
def load_data(folder_path):
    texts = []
    for filename in os.listdir(folder_path):
        if filename.endswith('.txt'):
            with open(os.path.join(folder_path, filename), 'r', encoding='utf-8') as f:
                texts.append(f.read())
    return texts
