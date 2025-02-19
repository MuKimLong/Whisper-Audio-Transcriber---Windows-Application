# Whisper-Audio-Transcriber---Windows-Application
Voice to text app


### Whisper Audio Transcriber - Windows Application

This project is a Python application that uses the Whisper model to transcribe audio files into text. The application accepts audio files, converts them, then transcribes them and saves the text as a Word document.

### Features
Faster Processing: Optimizations such as GPU acceleration, FP16 (Half Precision), and multithreading have been applied to improve processing speed.
Audio Conversion: FFmpeg is used to convert audio files to 16kHz for better Whisper model performance.
Simple Interface: A user-friendly GUI built with Tkinter for file upload and saving the transcription.
Output as Word: The transcribed text is saved as a Word document.
Requirements
Python 3.x
torch (PyTorch)
whisper (OpenAI's Whisper model)
tkinter (for GUI)
python-docx (to create Word documents)
ffmpeg (for audio conversion)
A system with a GPU (optional, for performance improvements)


### Installing Dependencies:
### Install Python Packages:


pip install torch whisper python-docx tkinter

### Install FFmpeg:

Download FFmpeg and install it on your system.

#### Ensure FFmpeg is installed by running the following command in your terminal or command prompt:

ffmpeg -version

### Run the Application:

Run the whisper_transcribe.py file to launch the application.

python whisper_transcribe.py

### Select an Audio File:

Click the "Select File" button in the main window to choose an audio file.
Supported file formats: .mp3, .wav, .m4a

### Transcribe:

The selected audio file will be converted and transcribed. A progress bar will show the ongoing process.

### Save the Results:

The transcribed text will be saved as a Word document. The file name is automatically set to the audio file's name, and the text will be split into paragraphs and saved.
Detailed Explanation of the Code
GPU Usage: If a GPU is available, the model is moved to the GPU, and the processing is done in FP16 format, which speeds up the process.

Audio Conversion: FFmpeg is used to convert the audio file to 16kHz. This helps Whisper process the audio more effectively.

Multithreading: Multithreading is used to perform the transcription in the background, ensuring the Tkinter GUI does not freeze during the process.

Tkinter GUI: The application features a simple GUI, where users can upload and save files. A progress bar indicates the status of the transcription process.

Converting to a Windows Application
To convert this Python script into a Windows application, follow these steps:

### Package with PyInstaller:

PyInstaller can be used to turn the Python script into a standalone Windows application. First, install PyInstaller:

pip install pyinstaller

Package the Application:

To convert whisper_transcribe.py into a .exe file, run the following command:


pyinstaller --onefile --windowed whisper_transcribe.py
--onefile: Packages everything into a single .exe file.
--windowed: Prevents a console window from showing when running a Tkinter GUI application.

FFmpeg Considerations:

To include FFmpeg with your Windows application, you can place the FFmpeg .exe file in the same directory as the generated .exe.
Alternatively, add FFmpeg to the system's PATH to ensure it's accessible to the application.
Distributing the Application:

PyInstaller creates a standalone .exe file for your application. You can distribute this file to any Windows machine to run the application without requiring Python to be installed.

Contributing
To contribute to this project, please follow these steps:

Fork this repository.
Make your changes and create a pull request.
If your contributions are accepted, the project owner will be notified.

### Project Owner: Muhammet Uzun
