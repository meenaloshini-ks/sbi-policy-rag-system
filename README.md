# SBI Policy RAG System

A PDF-based question-answering chatbot built in Google Colab using SBI’s Doorstep Banking Policy Version 5.0.

## Source Document
The source PDF is included as `POLICY ON DSB SERVICES 5.0.pdf`.

Download this PDF from the repository and upload it when prompted in Google Colab.

## Technologies
- Python
- Google Gemini
- NumPy
- pypdf
- Google Colab

## Features
- Extracts text from the uploaded PDF.
- Creates 800-character chunks with a 150-character overlap.
- Generates 768-dimensional embeddings.
- Retrieves the top 3 relevant chunks using cosine similarity.
- Answers questions using only the retrieved text.
- Displays supporting chunk IDs and similarity scores.
- Responds “I could not find this in the document” when the answer is unavailable in the retrieved context.

## Testing
The notebook includes:
- Three questions with answers in the PDF.
- Three questions with answers absent from the PDF.
- An experiment comparing 800-character and 3000-character chunks.

## Experiment Results
- 800-character chunks: 40 chunks.
- 3000-character chunks: 10 chunks.
- Smaller chunks answered all three in-document questions.
- Larger chunks answered two questions but missed the timeline question.

## How to Run
1. Open the notebook in Google Colab.
2. Add your Gemini API key to Colab secrets as `GEMINI_API`.
3. Run the cells in order.
4. Upload the SBI policy PDF when prompted.
5. Enter your questions.
6. Type `exit` to end each chat session.

## Purpose
An educational project demonstrating retrieval, embeddings, document-based answers, and the effect of chunk size.
