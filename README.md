# SpeechCNN
Kaggle Google TensorFlow Speech Recognition competition 

# Link
https://www.kaggle.com/c/tensorflow-speech-recognition-challenge

# Motivation
The competition's purpose is to build an algorithm that understands simple spoken commands. TensorFlow has released the Speech Commands Datasets. 
65,000 one-second long utterances of 30 short words, by thousands of different people. The challenge is to improve the recognition accuracy of
open-sourced voice interface tools. My own motivation is to get better acquainted with TensorFlow and using it to build neural nets and other
algorithms for data modeling. 

# Data
Test & Train data link:  https://www.kaggle.com/c/tensorflow-speech-recognition-challenge/data

Test Data
train.7z - Contains a few informational files and a folder of audio files. The audio folder contains subfolders with 1 second clips of voice
commands, with the folder name being the label of the audio clip. There are more labels that should be predicted. The labels you will need to
predict in Test are yes, no, up, down, left, right, on, off, stop, go. Everything else should be considered either unknown or silence. The 
folder _background_noise_ contains longer clips of "silence" that you can break up and use as training input.

The files contained in the training audio are not uniquely named across labels, but they are unique if you include the label folder. For 
example, 00f0204f_nohash_0.wav is found in 14 folders, but that file is a different speech command in each folder.

The files are named so the first element is the subject id of the person who gave the voice command, and the last element indicated repeated 
commands. Repeated commands are when the subject repeats the same word multiple times. Subject id is not provided for the test data, and you 
can assume that the majority of commands in the test data were from subjects not seen in train.

You can expect some inconsistencies in the properties of the training data (e.g., length of the audio).

test.7z - Contains an audio folder with 150,000+ files in the format clip_000044442.wav. The task is to predict the correct label. Not all of 
the files are evaluated for the leaderboard score.

# Goal
The TensorFlow Audio Recognition tutorial achieved a baseline of 0.88 on the Speech Commands Dataset. My goal is to achieve >0.80 score.

# Note 
The current code/notebook utilizes Keras instead of direct TensorFlow api's. Working in a two step process, TF will be used in 
part 2. 

Link
https://www.tensorflow.org/versions/master/tutorials/audio_recognition
