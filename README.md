# Precondiction Inference Prediction
Using RoBERTa-large-MNLI model to decide whether the precondition will enable or disable the statement.

### Sentence pair encoder ###
The encoder is a bidirectional transformer encoder. It is based on a pre-trained RoBERTa-large-MNLI model. The sentence pairs are combined together into a single sequence where a special token [SEP] is added at the end of each sentence. And another special token [CLS] is added at the beginning of the sequence. 

### Training & Development ###
Evaluated the solution by using the trained model to predict the dev set and compare the result with the label given in the set and to calculate the accuracy. Some key hyper parameter values are: optimizer = AdamW optimizer, learning rate = 1e-5, batch size = 32. Fine-tuning the model by using the training data and validate by dev data, and terminated the training with a fixed epoch, which is decided based on dev set performance. 
