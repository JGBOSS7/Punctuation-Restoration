# Punctuation Restoration

This repo has a main.ipynb file with the code and a train.csv file which is required to run the .ipynb as it has the dataset.

## Dataset Creation

The dataset was created from the [NLP mental health conversations dataset](https://www.kaggle.com/datasets/thedevastator/nlp-mental-health-conversations/data) by taking the response column only. Data was cleaned and lowercase version of this was taken as ground truth and inputs were unpunctuated versions of the same text.

## Architecture

The model used was a pre-trained bert model from huggingface, which is a transformer based model already pre-trained on large data. The tokenizer used was BertTokenizer and it was taken from huggingface. An 80-20 split was made for train and test. The model was trained for 25 epochs with cross entropy loss.

## Observations

The loss reduced gradually with training but the results were still not good as seen in the ipynb. Further training could enhance performance but a bigger batch size requires more memory and hence training is a time consuming process.