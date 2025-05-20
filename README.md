A Simple RNN is a type of neural network designed for sequential data, where the output depends not only on the current input but also on previous inputs. It’s useful for tasks like text classification, sentiment analysis, and next-word prediction. In Keras, it’s implemented using an Embedding layer (to convert words to vectors), followed by a SimpleRNN layer (to capture sequence patterns), and a Dense layer (for classification).
rnn_assignment.py — Main Python script implementing both tasks.
classification_data.csv — CSV file containing labeled text data (format: "text,label").
science_corpus.txt — Plain text file containing scientific text for training a next-word generation model.
How the code run :- According to the layout, I have deployed the code in google colab step by step.
 Preprocessing Steps
Classification
Split text,label column into separate columns.
Tokenized the text and padded sequences to equal length.
Label-encoded the target values.
One-hot encoded the labels for multiclass classification.
Used train_test_split() to divide into training and test sets.
Generation
Lowercased the text corpus.
Tokenized the full text and created sequences of 10 input tokens + 1 target token.
One-hot encoded the target words.
Observations
Final Test Accuracy: ~<value> (fill in after training)
Simple RNN effectively learns to classify short texts based on the labeled dataset.
Adding layers or switching to LSTM/GRU could improve performance on more complex data.
Generates grammatically plausible phrases based on the scientific corpus.
Coherence improves with more training epochs and larger context windows.
Simple RNN can struggle with long-term dependencies — LSTM would be more robust.

