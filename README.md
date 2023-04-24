# Audio-Classification-using-Matched-Filtering
The repository reads an audio file and applies a matched filter technique to identify the notes in the audio.

The audio file is read using the scipy.io.wavfile module and stored in the variables Fs and data, which represent the sampling frequency and the audio data, respectively.

The code defines a rectangular pulse function called rect(t), which is used to create a pulse train with the desired note frequencies. The main() function initializes an array with the note frequencies and calculates the beats per second based on a given BPM value. Then, it sets the 8 kHz sampling frequency and creates a timebase to be about 1.2 beats wide for visualization.

The code then creates a figure window and initializes empty arrays to hold the matched filter outputs for each note and the classification decision at each timestep. The matched filter output for each note is computed using a convolution of the audio data with the pulse train and the Hilbert transform to extract the amplitude envelope of the resulting signal. The classification decision is made by finding the note with the maximum output at each timestep and converting it to a note name.

The code plots the matched filter output for each frequency note, the classification decision as a function of time, and the classification decision names. The matched filter output is plotted for each note frequency in a separate subplot, where the x-axis represents the time in samples, and the y-axis represents the amplitude of the output. 

The classification decision is plotted as a function of time, where the x-axis represents the time in samples, and the y-axis represents the index of the note. The classification decision names are also plotted as a function of time, where the x-axis represents the time in samples, and the y-axis represents the name of the note.

Overall, the output of the code is a set of plots that show the matched filter output for each frequency note, the classification decision as a function of time, and the classification decision names, which can be used to identify the notes in the audio.
