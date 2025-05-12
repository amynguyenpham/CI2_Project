# CI2_Project

Repo for CI2 Final Project

Source Data: https://huggingface.co/datasets/ucberkeley-dlab/measuring-hate-speech
Processed Source Data: train.csv, train_with_topics.csv, test_reddit.csv, test_youtube.csv
Training: 

Project_P(Y_X).ipynb: training using standard classifier using BERT (https://huggingface.co/docs/transformers/en/model_doc/bert) and trainer (https://huggingface.co/transformers/v3.1.0/training.html#trainer)

Project_P(Y__X,A).ipynb: training using standard classifier using BERT (https://huggingface.co/docs/transformers/en/model_doc/bert) and trainer (https://huggingface.co/transformers/v3.1.0/training.html#trainer)

P(Y_do(x))_Twitter_In_Domain.ipynb: in-domain classifier using P*(A) (FLAN-T5-BASE generator: https://huggingface.co/google/flan-t5-base) and P(Y| X,A) - Precomputed

P_(Y_do(x)_Youtube.ipynb: in-domain classifier using P*(A) (FLAN-T5-BASE generator: https://huggingface.co/google/flan-t5-base) and P(Y| X,A) - Precomputed

P_(y_do(x)_Reddit.ipynb: in-domain classifier using P*(A) (FLAN-T5-BASE generator: https://huggingface.co/google/flan-t5-base) and P(Y| X,A) - Precomputed

