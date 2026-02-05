# Sound2Swara
Overview

Carnatic music defines melody as smooth movements between pitches rather than distinct notes. In Carnatic music, a single "swara" is defined with movements such as oscillations, slides, and pitch curve called "gamakas." Conventional music analysis techniques using pitches are found to be insufficient.

This project entails the proposal of an AI-based system designed for the automatic detection of swara, responding to an essential musical question:

Considering the sound shape, which swara do you hear?

Instead of using the notes to analyze the static frequencies, the system relies on the dynamic analysis of the pitch contours to identify the swaras.

Object

Extracting continuous pitch contours using Carnatic music audio

Detect the tonic (shruti) automatically

Normalization 
Normalize pitch values based on the tonic

Segmenting Melodic Phrases with Pitch Dynamics

Swaras should be identified based on the behavior of the pitches

Lay groundwork for gamaka-conscious transcription and raga identification

Key Idea

A swara of Carnatic music is not a point—swara is an entity on a timeline.

This project models:

pitch motion,

stability,

oscillation

and directionality,

to infer swara identity from its shape rather than its frequency.
Methodology
1. Audio Preprocessing

Noise Reduction

Silence trimming

Framing using small hop sizes

2. Pitch Extraction

High resolution pitch tracking with YIN or CREPE algorithms

Generation of Continuous Pitch Contours

3. Tonic Detection

Pitch histogram analysis

Estimation of the most stable reference pitch (shruti)

4. Pitch Normalization

Conversions to Relative Values
Conversion from absolute frequency (Hz) to relative cents

Enables performer-independent analysis

5. Melodic Seg

Segmentation based on pitch slope, variance, and continuity

Separates steady regions from expressive movements

6. Swara Detection (AI Model)

Sequence-based Machine Learning Model: LSTM/CNN-LSTM

Input pitch contour segments

swara label (Sa, Ri, Ga, etc.)

Dataset

– Carnatic vocal recordings (alapana/kriti excerpts)

Limited raga set for controlled experiments

Tonic references verified manually (where possible)

⚠️ As copyright is a concern, the audio files cannot be included here.

Evaluation Metrics

Pitch accuracy (Cent Deviation)

Swara classification accuracy

Confusion Matrix Analysis

Qualitative Listening-based Validation

Tech Stack

Language: Python

Audio Processing: Librosa, Num

Machine Learning: TensorFlow / PyTorch

Visualization: Matplotlib

Development: Jupyter Notebook/VS Code
Sample Output

Pitch Contours Visualization
So

Detected swara timelines

Swara prediction confidence plots

(Example outputs will be added after training and evaluation.)

Applications

Intelligent Carnatic music learning tools

Automated music transcription systems

Raga recognition pipelines

Research in computational musicology

Future Work

Classification of Explicit Gamaka

Raga recognition using Swara-Gamaka Sequ

Explainable AI for Music Theory Analysis

Support for instrumental music (violin, veena)

References

A list of the most relevant references related to music information retrieval, Carnatic music analysis, and deep learning will be added here.

Author

Monish.P
B.Tech CSE AI

Research Interest: AI for Music & Signal Processing

Final Note In this project, Carnatic melody is not considered as data points, but as living motion. The goal here is not just accuracy—but musical understanding.
