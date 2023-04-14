# Humor-Detection-DistilBERT
Pre-trained DistilBERT for Humor Detection

**Task**

The objective of this assigment is to use a pre-trained BERT-based model that correctly classifies texts between humour and non-humour class.

## **Dataset Description**

The following dataset was proposed by Annamoradnejad et al. in Dec. 2022. [1]. This dataset was created only for humour detection task. You can use the following dataset available in Kaggle: https://www.kaggle.com/datasets/deepcontractor/200k-short-texts-for-humor-detection

The authors justify the creation of this dataset by pointing out that pre-existing datasets for humour detection binary task were not large and rich enough to allow for robust and generalisable training and performances.  The dataset was created from two different data sources, one with humour texts and one without. The first set of texts comes from the News Category Dataset, published under CC0 Public Domain, containing various textual information (categories, stories, urls etc.) from the Huffington Post from 2012 to 2018. These texts belong to different categories such as politics, welfare, economics and entertainment. The second group of texts comes from the Jokes dataset, collected from the Reddit2 community and containing jokes/humour short texts. 

Several pre-processing and filtering steps were applied on the following dataset. 
Some of the steps are: removal of duplicate texts, selection of pairs of texts (one from each group) with similar statistics, character length between 30 and 100 and a word length between 10 and 18, sentence case formatting. The final dataset contains 200k labelled short texts distributed equally between humour and non-humour. 

The application of other preprocessing techniques is left to the reader.

## **Setup**

The notebook is divided into two parts. In the first I train DistilBERT on the original data, while in the second I train DistilBERT on the original dataset on which I have applied a basic text preprocessing pipeline. I use `DistilBertTokenizerFast` as tokenizer and `DistilBertForSequenceClassification` as model from HuggingFace. I evaluate my performances calculating Accuracy and F1 Score. 

## Results

   | Version | Loss | Accuracy | F1 Score |
   | ------------------- | ------- | ------- |  ------- |
   | Version1 | 0.3428 | 0.9473 | 0.9475 |
   | Version2 | 0.0882 | 0.9886 | 0.9886 | 

## **How to Run the Code**

Unless otherwise specified in the notebook section all codes can be runned in Google Colaboratory platform. All notebooks all already setted to import the necessary packages and also in this way you can easily use a GPU!

## References

[1] Annamoradnejad, Issa, and Gohar Zoghi. "Colbert: Using bert sentence embedding for humor detection." arXiv preprint arXiv:2004.12765 1.3 (2020).

[2] Sanh, Victor, et al. "DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter." arXiv preprint arXiv:1910.01108 (2019).


