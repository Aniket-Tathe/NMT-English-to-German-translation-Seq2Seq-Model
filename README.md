 Here is an updated README with model accuracy and loss:

# Neural Machine Translation (NMT) - English to German

This project trains a sequence-to-sequence neural machine translation model to translate English text to German.

## Model Architecture
The model consists of:
- An LSTM encoder that encodes the input English text into a latent vector representation  
- An LSTM decoder that decodes the latent vector representation into German text

## Training Data 
The model is trained on the deu-eng parallel corpus containing 25,000 English-German sentence pairs.

## Preprocessing
The texts are preprocessed by:
- Cleaning and tokenization
- Creating vocabularies and one-hot encodings for the input and target texts 
- Padding the input sequences

## Model Training
The model is trained for 200 epochs with a batch size of 64. RMSprop optimizer and categorical cross entropy loss are used.

After 200 epochs:
- Training Accuracy: 82%
- Validation Loss: 28%

## Evaluation
- A validation split of 20% is used during training to monitor overfitting
- BLEU score can be used to evaluate the translation quality

## Inference
An inference function is created to map the input english text to decoded german text using the trained models. 

## Future Work
There is scope for improvement with hyperparameter tuning, using more data, and experimenting with deeper models. Attention mechanism can also be added to potentially improve translation quality.

## Usage
The model can be used by calling the `decode_sequence` method and passing the input text to get the german translation.
