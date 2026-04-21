Small Language Model (SLM) From Scratch
This project demonstrates how to build and train a Small Language Model (SLM) from scratch with a target parameter size of 50-60 million. The goal is to generate creative and coherent text based on specific input data.

🚀 Project Overview
The model is trained on the TinyStories dataset, which consists of synthetic short stories designed to be understood by 3 to 4-year-olds. By focusing on a constrained vocabulary, we can achieve impressive text generation results with a relatively small number of parameters.

🛠️ Tech Stack & Dependencies
The following tools and libraries are required to run this project:

Python

PyTorch (for model architecture and training)

Datasets (HuggingFace library to load TinyStories)

tiktoken (OpenAI’s fast BPE tokenizer)

NumPy (for efficient data handling)

tqdm (for progress tracking)

📋 Implementation Steps
1. Data Acquisition
We use the roneneldan/TinyStories dataset from HuggingFace. This dataset provides a high-quality, simplified linguistic environment ideal for training small-scale models.

2. Tokenization & Preprocessing
The text is processed using the gpt2 encoding via the tiktoken library.

Encoding: Sentences are converted into token IDs.

Efficiency: To handle the dataset efficiently without exhausting RAM, the tokenized data is stored on disk using numpy.memmap in train.bin and validation.bin files.

Algorithm: Byte Pair Encoding (BPE) is utilized to handle words, characters, and subwords.

3. Model Architecture (In Progress)
The model is designed to be a lightweight Transformer-based architecture optimized for creative text generation within a 50-60 million parameter budget.

⚙️ How to Run
Install Dependencies:

Bash
pip install datasets tiktoken numpy tqdm
Prepare the Data:
Run the preprocessing cells in the notebook to download and tokenize the dataset. This will generate train.bin and validation.bin.

Train the Model:
Follow the training loop sections in the notebook to begin the optimization process.
