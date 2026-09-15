# Assignment 13: Generative AI Essentials

**Name:** OBAJE PAUL
**Course:** MACHINE LEARNING

## Overview

This project explores the basic concepts of Generative Artificial Intelligence, with a focus on text generation and Generative Pre-trained Transformers (GPTs).

The practical part of the assignment uses a publicly available text from Project Gutenberg to train a basic character-level text generation model using Python and TensorFlow/Keras.

An LSTM (Long Short-Term Memory) neural network is used to learn patterns from the training text and generate new text based on a seed input.

The project also explains GPT architecture, tokenization, attention mechanisms, probability-based text generation, applications of Generative AI, and ethical considerations.

## Dataset

The dataset used in this project is the text of:

**Alice's Adventures in Wonderland by Lewis Carroll**

The text is obtained from Project Gutenberg, a collection of freely available eBooks and public-domain works.

The dataset is downloaded directly from the notebook, so a separate dataset file is not required to run the project.

## Dataset Preparation

The text is prepared before training by:

* Converting the text to lowercase
* Removing unsupported characters
* Selecting a manageable portion of the text
* Identifying unique characters
* Converting characters into numerical values
* Creating sequences for model training

A character-level approach is used, meaning that individual characters rather than complete words are used as the basic units.

The model uses sequences of 40 characters to predict the next character.

## Model Implementation

The practical generative model is an LSTM neural network developed using TensorFlow/Keras.

The model contains:

* An Embedding layer
* An LSTM layer with 128 units
* A Dense output layer
* Softmax activation for producing probabilities for possible characters

The model is trained using sparse categorical cross-entropy loss and the Adam optimizer.

## Text Generation

After training, the model generates text by receiving a seed input and predicting the next character.

The predicted character is added to the sequence, and the updated sequence is used to predict the next character. This process continues until the requested amount of text has been generated.

Different seed inputs are tested to demonstrate how the starting text can influence the generated output.

## Practical Application

A simple creative content-generation application is demonstrated.

The application accepts a short seed phrase such as:

```text
once upon a time
```

and generates a continuation using patterns learned from the training text.

This demonstrates a basic example of how Generative AI can be used as a creative writing assistant.

## GPT Architecture

The project also provides an overview of Generative Pre-trained Transformers (GPTs).

GPT models are based on the Transformer architecture and use self-attention mechanisms to process relationships between tokens in a sequence.

The general process can be summarized as:

```text
Text
↓
Tokenization
↓
Token Embeddings
↓
Transformer Self-Attention
↓
Probability Distribution
↓
Next Token
↓
Updated Sequence
```

GPT models are trained using next-token prediction. During generation, the model repeatedly predicts the next token based on the context provided by the previous tokens.

The practical model in this project uses an LSTM rather than a Transformer because the aim is to demonstrate the fundamental concept of text generation using a model that can be trained efficiently in Google Colab.

## Findings

The trained LSTM model was able to learn character-level patterns from the selected text and generate new sequences based on seed inputs.

The generated text demonstrated some patterns from the training data, including spelling and punctuation patterns. However, some generated sequences contained grammatical errors, repetition, or incomplete ideas.

This is expected from a small model trained on a limited amount of text. More advanced language models use much larger datasets and more complex architectures.

## Applications of Generative AI

Generative AI can be applied in areas such as:

* Content creation
* Education
* Programming assistance
* Customer service
* Marketing
* Creative writing
* Summarization
* Idea generation

Generative AI can improve productivity, but generated content should still be reviewed by humans.

## Ethical Considerations

Several ethical issues were considered in this project.

### Bias

Generative models can learn and reproduce biases present in their training data. Diverse and carefully reviewed training data can help reduce this problem.

### Misinformation

Generative AI can produce convincing content that is incorrect. Fact checking and human review are important when using generated information.

### Copyright

Generative AI raises questions about the ownership and use of training data and generated content. Using public-domain or appropriately licensed material is an important part of responsible AI development.

### Privacy

Training data can contain personal information. Data should be handled responsibly and unnecessary sensitive information should be removed.

### Human Oversight

Important decisions should not rely entirely on automatically generated content. Human supervision remains important when AI systems are used in real-world applications.

## Technologies Used

* Python
* Google Colab
* TensorFlow/Keras
* NumPy
* Matplotlib
* Requests

## How to Run

1. Open the Jupyter Notebook in Google Colab.
2. Run the cells from top to bottom.
3. The notebook downloads the Project Gutenberg text automatically.
4. The text is cleaned and converted into numerical sequences.
5. The LSTM model is created and trained.
6. Training loss is visualized.
7. Seed inputs are used to generate new text.
8. The creative content-generation example is demonstrated.
9. The notebook also contains explanations of GPT architecture, applications, and ethical considerations.

## Project Files

**Assignment_13_Generative_AI_Essentials_OBAJE_PAUL.ipynb**
Contains the complete Google Colab implementation, documentation, model training, visualizations, text generation, practical application, and discussion.

**Assignment_13_Generative_AI_Essentials_OBAJE_PAUL.pdf**
PDF version of the completed notebook for assignment submission.

**README.md**
Provides an overview of the project, dataset, methodology, technologies, and instructions for running the notebook.

## Conclusion

This project demonstrates the basic principles of Generative AI and text generation using an LSTM model. A publicly available Project Gutenberg text was processed and used to train a character-level model capable of generating new text from seed inputs.

The project also explains how GPT models use tokenization, embeddings, self-attention, probability distributions, and next-token prediction to generate text.

The practical experiment shows both the potential and limitations of small generative models. While the model can learn patterns from text and produce new sequences, higher-quality generation requires larger datasets, more advanced architectures, and greater computational resources.

**Author:** OBAJE PAUL
**Course:** MACHINE LEARNING

