# VOICE-QUERY-ASSISTANT-using-SV2TTS
Voice query assistant to request and receive information about a course, such as, professor's contact information, course schedule, exam and assignment dates and grading, etc. It also includes a voice cloning feature that allows to reproduce the answer of the query with the corresponding professor's voice. This is done using the SV2TTS tool by Corentin Jemine (https://github.com/CorentinJ/Real-Time-Voice-Cloning).

1. Install Requirements

Python 3.7 is needed to run the tool

Speech Recognition:
pip install SpeechRecognition
pip install pydub
pip install pyaudio

SV2TTS:
#Clone repository
git clone https://github.com/CorentinJ/Real-Time-Voice-Cloning.git
#Select directory
cd Real-Time-Voice-Cloning/
#Install Pytorch
pip install torch torchvision
#Install requirement and dependencies
pip install -r requirements.txt
#Download pretrained data and unzip it
gdown https://drive.google.com/uc?id=1n1sPXvT34yXFLT47QZA6FIRGrwMeSsZc
unzip pretrained.zip
Move these files into Real-Time-Voice-Cloning/

2. Code configuration
In the code, some configurations are needed:
Line 346: The parameter "minutes" represents the duration of the reference voice sample that wants to be used to clone the voice. Choose between: 5,15,30,45,60.
Line 389: Choose filename where the generated cloned answer will be saved.

3. Launch Voice Query assistant
py voice_assistant.py

The user will ask one of the possible fifteen questions (available in "Questions.pdf" in "Sillabi & Questions" folder) and this will be captures by the microphone. After performing the SQL query, the answer will be reproduced with the corresponding proffesor's cloned voice.

4. Test similarity with Resemblyzer
The Python package Resemblyzer allows to compare and analyze the cloned voices and the real ones. It provides several demos explained at: https://github.com/resemble-ai/Resemblyzer

#Install package
git clone https://github.com/resemble-ai/Resemblyzer.git
pip install resemblyzer
