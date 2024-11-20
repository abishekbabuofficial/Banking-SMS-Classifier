# Banking-SMS-Classifier
The repository explains and provides resources to build a BERT Text Classifier that classifies the SMS text into Banking or Non-Banking messages. It uses BERT pre-processor and BERT encoder.

### Try out the Working Model: https://huggingface.co/spaces/abishek-official/Bert_Text_Classification

## Dataset
Due to privacy reasons dataset for classifying Banking(Ham) and Non-Banking(Spam) messages are not published. Steps to prepare dataset follows:
**Step 1:** Collect the necessary Banking and Non-Banking messages from different user with diversity in banks and include also some SPAM data as Non-Banking for accuracy.

**Step 2:** Categorize the messages as Banking and Non-Banking in seperate column as shown below

![image](https://github.com/user-attachments/assets/d1dc0f12-1fe9-4ad8-9ced-cd49cf038db4)

**Step 3:** The code for downsampling the data is given in the notebook which downsamples the excess data and prevents overfitting.


## What is BERT pre-processor?

**The BERT preprocessor in text classification prepares raw text data for input into a BERT model. It performs the following key tasks:**

**Tokenization:** Splits text into subword tokens using WordPiece or SentencePiece.
**Adding Special Tokens:** Inserts [CLS] (classification token) at the start and [SEP] (separator token) at the end of the sequence.
**Truncation/Padding:** Adjusts sequence length to fit the model's fixed input size.
**Converts to IDs:** Maps tokens to their corresponding numerical IDs from BERT's vocabulary.
**Generates Attention Masks:** Creates masks to indicate real tokens (1) versus padding (0). In our case 1-Banking Message, 0-Non Banking Message.

## What is BERT?
BERT models are pre-trained on a large corpus of text (for example, an archive of Wikipedia articles) using self-supervised tasks like predicting words in a sentence from the surrounding context. This type of training allows the model to learn a powerful representation of the semantics of the text without needing labeled data.

## What is BERT encoder?
The BERT encoder is the core component of the BERT model, responsible for transforming tokenized text into meaningful vector representations (embeddings). It consists of multiple layers of transformer blocks that leverage self-attention mechanisms and feed-forward neural networks.

### What It Does:
**Contextual Embeddings:** Encodes each word in the text while considering its surrounding context, capturing the meaning of words with others.
**Positional Awareness:** Includes positional embeddings to understand the order of tokens in the sequence.
**Bidirectional Understanding:** Reads the text both forward and backward, enabling deep context understanding.

**Note:** Here we used Encoder model - https://tfhub.dev/tensorflow/bert_en_uncased_L-12_H-768_A-12/4

## Flowchart of the project
![image](https://github.com/user-attachments/assets/dcedfb4b-c723-4c85-bf19-9b209e18c86b)


##For Official Documentation Reference
https://www.tensorflow.org/text/tutorials/classify_text_with_bert

#Thank You for Reaching out to my Repository
