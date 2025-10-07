# [TM&NLP] Project Submission 2024–2025 – *TweetToneClassifier*
The project was made by me (Diego Meloni) in collaboration with a university colleague (Brusamarello Michelangelo).

## Goal

The objective of this project is to build a classifier that detects the **tone of tweets**, classifying them into one of four categories:

-  **Regular**
-  **Ironic**
-  **Sarcastic**
-  **Figurative** (both ironic and sarcastic)

Further considerations about the project and the dataset can be found in the notebook and in the reports.

---

## Requirements

- A **Google Account** (for Google Colab and Google Drive)
- **Dataset** from Kaggle:  
  [Tweets with Sarcasm and Irony](https://www.kaggle.com/datasets/nikhiljohnk/tweets-with-sarcasm-and-irony)
- **Pre-trained LLM:** [Microsoft Phi-3-mini-128k-instruct](https://huggingface.co/microsoft/Phi-3-mini-128k-instruct)

>  **Note:** The Phi-3 model is automatically downloaded the first time the program is executed.  
> You don’t need to download it manually — doing so might even cause conflicts.

---

## Dataset Setup

We use **Google Drive** to import the dataset during runtime in Google Colab.

### Steps:
1. Create a folder in your Google Drive named **exactly**: "Text Mining project"
2. 2. Download the dataset from Kaggle.
3. Place the files inside that folder with the following names:
- `train.csv` (training set)
- `test.csv` (test set)

The project code automatically accesses the dataset from:
/content/drive/MyDrive/Text Mining project/train.csv
/content/drive/MyDrive/Text Mining project/test.csv


---

##  Library Installation

Google Colab already includes many preinstalled libraries (like `tensorflow` and `scikit-learn`),  
but you still need to install the following:

```bash
!pip install bitsandbytes --prefer-binary
!pip install huggingface_hub
!pip install nltk
!pip install gensim
!pip install transformers==4.48.0
```
Important: After installing transformers, restart the Colab runtime.
This version may have limited compatibility with certain libraries.
