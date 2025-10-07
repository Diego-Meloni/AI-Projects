# [TM&NLP] Project Submission 2024–2025 – *TweetToneClassifier*
The project was made by me (Diego Meloni) in collaboration with a university colleague (Brusamarello Michelangelo).

## Goal

The objective of this project is to build a classifier that detects the **tone of tweets**, classifying them into one of four categories:

-  **Regular**
-  **Ironic**
-  **Sarcastic**
-  **Figurative** (both ironic and sarcastic)

During the project we encountered many challenges and problems of different nature:
- Tweets contain internet slang, hashtags (united words with no separating space), mentions, urls and emojis.
- Resources constraints: Since we needed to make our project using Google Colab, we had to avoid heavy datasets and dictionaries, and even our models and embedding had to be limited to make the project run better.
- Libraries conflict: Google Colab comes with some preinstalled libraries, but at some point the versions in some of these libraries are in conflict, 
so in order to run the last part of the code you need to restart the session and to launch the first part until after the data preprocessing, to then directly use the transformers part for the LLM prompting. 
- The very nature of the dataset: There is no clear cut distinction between irony, sarcasm, and when they are both applied.
  The line is blurry even for humans, and the classification could contain biases caused by subjectivity.

Further considerations about the project and the dataset can be found in the notebook and in the reports.

---

## Requirements
The notebook is self containted, meaning it is possible to directly run it without doing setup procedures or downloading unnecessary files.
- **Dataset** from Kaggle (loaded from GitHub):  
  [Tweets with Sarcasm and Irony](https://www.kaggle.com/datasets/nikhiljohnk/tweets-with-sarcasm-and-irony)
- **Pre-trained LLM:** [Microsoft Phi-3-mini-128k-instruct](https://huggingface.co/microsoft/Phi-3-mini-128k-instruct)

>  **Note:** The Phi-3 model is automatically downloaded the first time the program is executed.  
> You don’t need to download it manually

---

##  Library Installation

Google Colab already includes many preinstalled libraries (like `tensorflow` and `scikit-learn`),  
but you some still need to be installed to run the project:

```bash
!pip install bitsandbytes --prefer-binary
!pip install huggingface_hub
!pip install nltk
!pip install gensim
!pip install transformers==4.48.0
```
> Important: After installing transformers, restart the Colab runtime.
> This version may have limited compatibility with certain libraries.

---

