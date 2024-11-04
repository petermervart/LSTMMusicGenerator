# Generating Music with LSTM

This project demonstrates the use of a Long Short-Term Memory (LSTM) network to generate music. The model is trained on a dataset of MIDI files and learns to predict the next note in a sequence, given a previous sequence of notes.

Detailed explanation with visualizations in jupyter notebook: [Notebook](MusicGenerator.ipynb)

**Key Steps:**

1. **Data Preparation:**
   - MIDI files are parsed to extract notes and their corresponding features (pitch, duration, and step).
   - The data is preprocessed and formatted into sequences suitable for training the LSTM model.

2. **Model Architecture:**
   - A single-layer LSTM network is used to process the input sequences.
   - The model has three output layers: one for predicting pitch, one for predicting step, and one for predicting duration.
   - Custom loss functions are employed to optimize the training process.

3. **Training:**
   - The model is trained on the prepared dataset using an appropriate optimizer and loss function.
   - Early stopping is implemented to prevent overfitting.

4. **Music Generation:**
   - Given a seed sequence of notes, the model generates new notes one at a time.
   - The predicted note is added to the input sequence, and the process is repeated to generate a longer musical piece.

5. **Output:**
   - The generated notes are converted back to a MIDI file, which can be played using a MIDI player.

## Key Takeaways:

- LSTM networks are effective for modeling sequential data, such as music.
- Careful data preparation and feature engineering are crucial for successful model training.
- Experimentation with hyperparameters and model architectures can improve the quality of generated music.

## Future Work:
- Explore different LSTM architectures, such as stacked LSTMs or bidirectional LSTMs.
- Incorporate additional features, such as tempo and dynamics, to enhance the generated music.
- Implement techniques like beam search or sampling to generate more diverse and creative music.
