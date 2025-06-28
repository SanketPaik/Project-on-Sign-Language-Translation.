# Real-Time Sign Language Detection Web App

This project is a Flask-based web application that enables real-time detection and translation of American Sign Language (A–Z) using a webcam. It utilizes MediaPipe for hand landmark detection and a pre-trained deep learning model (`combined_aaa.keras`) for sign recognition.

## 🌟 Features

- 📷 **Real-Time Sign Detection** using webcam
- 🧠 **Trained Neural Network Model** for 26 alphabets (A–Z)
- ✋ **MediaPipe Hands** for landmark extraction
- 💬 **Two Modes**: 
  - **Sign Mode**: Detects and displays a single alphabet
  - **Sentence Mode**: Continuously forms words/sentences from hand gestures
- 💾 **Data Collection Tools** for capturing training data
- 🖼️ Visual reference for signs via `signs.png`
- 🔠 Space, delete last letter, and clear sentence functionalities
- 🖥️ Simple and interactive HTML frontend

---

## 📁 Project Structure

├── data_collection.py # Script to collect hand sign images and landmark data
├── to_create_csv.py # Converts sign images into CSV format using MediaPipe
├── combined_aaa.keras # Trained ML model for hand sign classification
├── test_model.py # Flask server to run the application
├── index.html # Main web interface
├── shutdown.html # Page displayed after shutting down the server
├── signs.png # Sign language reference image
├── static/ # Static files (include signs.png here)
├── templates/ # Flask HTML templates
│ ├── index.html
│ └── shutdown.html

 How to Run

Make sure your webcam is connected.
Place the combined_aaa.keras model and signs.png inside appropriate folders.
Run the Flask application:
python test_model.py
Your browser will automatically open at http://127.0.0.1:5000.

Controls
Modes
Click "Detect Single Sign" to display individual letters.

Click "Detect Sentence" to construct full sentences.

Keyboard Shortcuts (in Sentence Mode)
Press E → Clear full sentence

Press C → Delete last character

Press Space button → Add space between words.


📊 Data Collection (Optional)
To collect your own dataset:

Run data_collection.py

Follow on-screen instructions to capture sign images

Use to_create_csv.py to generate labeled CSV data

🤖 Model Training (Optional)
This project uses a pre-trained model (combined_aaa.keras). You can retrain the model using the CSV file created from your collected data.

🛑 Shutdown
Click Exit on the web page or stop the terminal. You will see a shutdown confirmation page (shutdown.html).

📌 Credits
MediaPipe: For hand tracking

TensorFlow / Keras: For deep learning model

OpenCV: For image capture and frame processing

Flask: For backend web server

Requirment.txt
flask
opencv-python
mediapipe
tensorflow
numpy
pandas

