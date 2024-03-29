# Using-LSTMS-for-Polyphonic-Music-Generation-with-the-JSB-Chorales-Dataset

The included files were used in my dissertation, Using LSTMs for Polyphonic Music Generation with the JSB Chorales Dataset.
The aim of this project was to integrate a polyphonic dataset with an LSTM music system for polyphonic music generation.

This project introduces two new methods for encoding polyphonic music.
The Duration encoding has 3 columns, the first is the onset of the note (in semiquaver beats), the second is the duration of the note (in semiquaver beats and the third is the MIDI note number.
The Off encoding also has 3 columns, the first is the onset of the note (in semiquaver beats), the second is the offset of the note (in semiquaver beats) and the third is ht MIDI note number. 

generate_data.m takes the MIDI dataset and encodes it using both the duration and off encoding methods.
The encoded JSB chorales dataset is contatined, split into training, validation and testing sets.

Neural_Network.py splits the data to be used, for input into the LSTM network. A model is set up and trained. Music is generated based on the given MIDI input.

overfitting_similarity.m is used to objectively assess the output of the system. To test for overfitting, the output is compared to the training data. 
To test for similarity, the output is compared to the Bach piece which in the input came from.

The musical clips that were used in the listening tests can be found in the folder Listening_Test_clips
