# Generating Music with LSTM

This notebook demonstrates how to generate music using Long Short-Term Memory (LSTM) neural networks, specifically processing MIDI files to create a dataset for training.

Detailed explanation with visualizations in jupyter notebook: [Notebook](MusicGenerator.ipynb)

## Installation of Required Libraries
The following libraries are installed for MIDI file processing and model training:
- fluidsynth
- pyfluidsynth
- pretty_midi
- wandb

## Importing Libraries
The necessary libraries such as `numpy`, `pandas`, `tensorflow`, and others are imported to facilitate data handling and model building.

## Weights and Biases Initialization
Wandb is initialized for logging and tracking the model's performance during training.

## MIDI File Processing
The notebook processes MIDI files to extract notes and their attributes:
- Instruments are identified and counted to determine the most common instrument.
- MIDI files are converted to a structured format of notes, capturing attributes such as pitch, step, and duration.

## Data Visualization
Visualizations are created to show:
- The piano roll of the first 1000 notes.
- Histograms of pitch, step, and duration features to understand their distributions.

## Dataset Preparation
The dataset is transformed into sequences suitable for LSTM input, with a defined sequence length and vocabulary size. A custom loss function is defined to handle predictions more effectively.

## Model Architecture
A single-layer LSTM model is defined with three outputs representing pitch, step, and duration. The model is compiled with a combination of loss functions and weights to optimize training.

## Training
The model is trained with callbacks for checkpointing and early stopping, allowing it to learn the patterns in the music data over multiple epochs.

## Music Generation
After training, the model is used to generate new notes based on a starting sequence. The generation process includes randomness controlled by a temperature parameter.

## MIDI File Output
Finally, the generated notes are converted back to a MIDI file format using PrettyMIDI for playback.

This notebook provides a comprehensive approach to generating music using machine learning, specifically showcasing the power of LSTMs in learning from sequential data.
