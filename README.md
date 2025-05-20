# Regulation Requirement Extractor

A Streamlit-based application to extract system-level requirements from technical PDF documents using OpenAI GPT models and LangChain semantic search.

## Features

- **PDF Upload**: Upload and analyze technical or system requirement documents in PDF format
- **Document Classification**: Verifies if the uploaded file is a requirement document using GPT-3.5
- **Requirement Extraction**: Translates technical content into clear, actionable system requirements
- **Semantic Search**: Uses LangChain and embeddings to locate the most relevant document sections
- **Excel Export**: Outputs requirements in a downloadable Excel file
- **Temporary File Handling**: Automatically cleans up uploaded and generated files after use

## Screenshots

### User Interface – Upload and Analysis
![Streamlit UI](https://github.com/user-attachments/assets/b490088a-b477-44df-8262-21fd8f5bbfbc)

### Output – System Requirements Excel
![Excel Output](https://github.com/user-attachments/assets/54cc7224-d0d2-49c2-992f-de1f79af69d9)

## Dependencies

- [Streamlit](https://streamlit.io/)
- [OpenAI Python SDK](https://pypi.org/project/openai/)
- [LangChain](https://www.langchain.com/)
- [PyMuPDF (fitz)](https://pymupdf.readthedocs.io/en/latest/)
- [Pandas](https://pandas.pydata.org/)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Regulation_Extractor
   cd Regulation_Extractor
2. Install required packages:
   
```bash
   pip install -r requirements.txt
   ```

3. Set up your OpenAI API key:
   - Create a `.streamlit/secrets.toml` file with your API key:
     ```toml
     OPENAI_API_KEY = "your-openai-api-key-here"
     ```

## Usage

1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

2.Upload a PDF requirement or technical document

3.Let the app analyze and validate the document type

4.If valid, the app will extract the most relevant system requirements

5.Download the generated Excel file with the requirements


## Development
This application uses:

- LangChain: For semantic search and document chunking

- OpenAI GPT-3.5: For requirement classification and rewriting

- PyMuPDF: To extract text from uploaded PDF documents

- Streamlit: To build an interactive web UI

To Extend the App
- Modify the prompt templates to better suit your specific domain or project

- Customize the vector search query or adjust k in similarity search

- Support additional file formats like .docx or .txt

- Integrate a persistent vector database (e.g., FAISS or Chroma)
