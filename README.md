Cloningshazam

Cloningshazam is a Python project that processes subtitle data from a SQLite database, cleans and chunks the text, and stores embeddings in a ChromaDB collection. It then leverages Whisper for audio transcription and a SentenceTransformer model to perform similarity searches against the stored subtitle embeddings.

Features

Subtitle Extraction: Reads and decodes subtitle data from a zipped SQLite database.

Text Preprocessing: Cleans text by lowering case, removing numbers and special characters, and filtering out stopwords.

Text Chunking: Splits long texts into overlapping chunks to preserve context.

Audio Transcription: Uses the Whisper model to convert audio files into text.

Embedding and Search: Converts text chunks to embeddings using SentenceTransformer, stores them in ChromaDB, and retrieves relevant results via a TF-IDF and embedding-based search.

Setup

Install Dependencies:

pip install nltk pandas chromadb sentence-transformers whisper scikit-learn openai-whisper

Download NLTK Resources:

The script downloads necessary NLTK data (e.g., stopwords) on first run.

Google Drive Integration:

If running in Colab, the project mounts Google Drive to access the database file.

Usage

Extract Subtitles: Reads a specified database file and samples subtitle data.

Store Embeddings: Cleans and chunks the subtitle text, encodes them into embeddings, and stores them in a ChromaDB collection.

Search Subtitles: Transcribes an input audio file and queries the stored embeddings to return the most relevant subtitle snippets.

Simply run the script to see a sample search result printed to the console.

This project provides a lightweight yet powerful framework to combine audio transcription with subtitle search, similar in spirit to Shazam's audio recognition, but applied to subtitle data.
