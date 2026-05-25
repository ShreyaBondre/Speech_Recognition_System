# Speech_Recognition_System

*COMPANY*: CODTECH IT SOLUTIONS

I*NAME*: Shreya Vilas Bondre

 *INTERN ID*: CTIS7717

*DOMAIN*: Artificial Intelligence

 *DURATION*: 8 WEEEKS

 *MENTOR*: NEELA SANTOSH
 The given Python program is a Speech Recognition System developed using Python in Google Colab. The main purpose of this code is to convert speech from an audio file into text automatically using Google Speech Recognition API.

At the beginning of the program, the required libraries such as SpeechRecognition, pydub, requests, and io are imported. The pip install command is used to install the necessary packages inside Google Colab.

The program defines a function named transcribe_audio_from_url(audio_url) which accepts the URL of an audio file as input. Inside this function, the audio file is downloaded directly from the internet using the requests library. A User-Agent header is added to the request so that the server treats the request like a normal web browser request.

The downloaded audio data is stored in memory using BytesIO, which avoids saving the file physically on the computer. The program checks whether the file format is WAV or MP3 based on the URL extension. Then, the pydub library converts the audio into WAV format because the SpeechRecognition library works properly with WAV audio files.

After conversion, the audio is loaded into the Speech Recognition engine using sr.AudioFile(). The recognizer adjusts for background noise using the adjust_for_ambient_noise() method and records the complete audio using record().

The recorded audio is then sent to the Google Speech Recognition API using the recognize_google() method. The API processes the speech and converts it into text format. The final transcribed text is returned and displayed as output.
