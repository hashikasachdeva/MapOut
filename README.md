# MapOut
This project is an intelligent question-answering system capable of handling both text and audio queries. It utilizes various pre-trained models and libraries to perform question-answering, text-to-speech conversion, speech-to-text recognition, and PDF text extraction.
**
Setup and Running Instructions**
Prerequisites
Ensure Python 3.7 or higher is installed on your system. You also need pip to install Python packages.

**Install Required Packages:**
pip install numpy faiss-cpu transformers sentence-transformers SpeechRecognition gTTS pdfplumber

**Prepare the PDF Document:**
Place your PDF document in the /content/ directory. The default file name expected is Career Counseling Training Guide 2023 - 24 - FREE E-Book.pdf. Modify the document_path variable in the script if your file name or location differs.

**Prepare an Audio File for Testing:**
If testing audio-based queries, ensure you have an audio file named question.wav placed in the /content/ directory or adjust the path in the script accordingly.

This script will perform the following actions:

Test a text-based query.
Convert the answer to speech and save it as output.mp3.
Test an audio-based query (assuming the audio file question.wav is present).

**Models and Libraries Used**
1. Question-Answering Model:

    Model: deepset/roberta-base-squad2
    Library: transformers
    Purpose: This model extracts answers from text paragraphs based on user questions.
   
2. Sentence Embedding Model:

    Model: all-MiniLM-L6-v2
    Library: sentence-transformers
    Purpose: This model generates vector embeddings for text paragraphs, enabling similarity searches using FAISS.
   
**Libraries**
NumPy:
Purpose: Provides support for array operations and numerical computations.

FAISS:
Purpose: Facilitates efficient similarity search and clustering of vector embeddings.

SpeechRecognition:
Purpose: Converts spoken language from audio files to text.

gTTS (Google Text-to-Speech):
Purpose: Converts text to speech and saves it as an audio file.

pdfplumber:
Purpose: Extracts text from PDF files.

**Testing**
1. Text Query Test:
    The script tests a predefined text-based question and prints the answer.
    The answer is also converted to an audio file named output.mp3.

2. Audio Query Test:
    The script processes an audio file named question.wav and attempts to provide an answer based on its content.
    License
    This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For questions or issues, please contact [hashika.sachdeva17@gmail.com].


