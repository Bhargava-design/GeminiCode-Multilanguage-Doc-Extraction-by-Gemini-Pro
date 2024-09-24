### Project Documentation: GeminiDecode - Multilanguage Document Extraction by Gemini Pro

---

Doc: [SI-5283-1727165652.pdf](https://github.com/user-attachments/files/17113885/SI-5283-1727165652.pdf)

Video_Link: https://youtu.be/2J4hEE8cBoI?feature=shared

 
#### 1. **GeminiDecode: Multilanguage Document Extraction by Gemini Pro**

"GeminiDecode" is a project focused on extracting, processing, and querying text from PDFs in multiple languages using Google's Gemini Pro AI model. The core goal is to allow users to upload PDF documents in any language, process the text content, store it, and ask questions based on the extracted information. The system then uses a combination of machine learning and natural language processing (NLP) to generate answers from the context of these documents.

**Key Features:**
- Supports PDF documents in various languages.
- Uses Google’s Gemini Pro model for document text extraction and query generation.
- Vector-based similarity search ensures relevant responses to user questions.
- Embedding support via LangChain and FAISS (Facebook AI Similarity Search).

---

#### 2. **Requirements, Specifications, Technologies, and Libraries**

**Requirements:**
- Extract text from PDFs in multiple languages.
- Allow users to ask questions related to the documents uploaded.
- Generate answers based on the content of the documents.
- Save and retrieve embeddings for document text using a vector search.

**Specifications:**
- Handle PDFs of various sizes and content structures.
- Chunk text for efficient processing.
- Search for relevant context based on user queries.
- Multilanguage support for text extraction and question-answering.
  
**Technologies:**
- **Streamlit**: For building the user interface and managing file uploads.
- **Google Generative AI**: Specifically, the Gemini Pro model for text extraction and question generation.
- **LangChain**: For managing text splitting, embeddings, and the question-answering chain.
- **FAISS**: For vector-based similarity search over the document content.
- **PyPDF2**: For extracting text from PDFs.
  
**Libraries Used:**
- `streamlit`: Interface for interacting with the system.
- `PyPDF2`: PDF reading and text extraction.
- `langchain.text_splitter`: Splitting large texts into chunks for efficient processing.
- `langchain_google_genai`: Integration with Google Generative AI models.
- `faiss`: Vector store to index and query document embeddings.
- `PIL`: For image processing (optional, depending on the Gemini model's capabilities).
- `dotenv`: To load environment variables, such as API keys.

---

#### 3. **Use of Google API Key**

The Google API key is required to access and interact with Google’s Gemini Pro AI model. It allows your code to authenticate with Google's cloud services and utilize their AI capabilities, including:
- Embedding creation: Generating vector representations of the document text for similarity searches.
- Question-answering: Using the Gemini model to answer user queries based on the context extracted from documents.

**Configuration:**
The API key is loaded via the `.env` file using `load_dotenv()` for security purposes, keeping the sensitive data out of your codebase.

---

#### 4. **Step-by-Step Commands Used in Terminal**

Here are the steps to set up and run the project locally:

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # For Windows use: venv\Scripts\activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create a `.env` file** in the project directory:
   ```bash
   touch .env
   ```

5. **Add the Google API key** to the `.env` file:
   ```bash
   GOOGLE_API_KEY=your-google-api-key-here
   ```

6. **Run the Streamlit application:**
   ```bash
   streamlit run main.py
   ```

---

#### 5. **Deployment on GitHub with Commands**

To deploy this project on GitHub:

1. **Initialize a Git repository:**
   ```bash
   git init
   ```

2. **Add files to the repository:**
   ```bash
   git add .
   ```

3. **Commit the changes:**
   ```bash
   git commit -m "Initial commit"
   ```

4. **Create a new repository on GitHub**, then link the local repository to the GitHub remote:
   ```bash
   git remote add origin <repository-url>
   ```

5. **Push the code to GitHub:**
   ```bash
   git push -u origin main
   ```

---

#### 6. **Guide to Download, Install, and Run the Code**

To run the "GeminiDecode" project on your local machine, follow these steps:

**Step 1**: Clone the project repository.
```bash
git clone <repository-url>
```

**Step 2**: Navigate to the project folder.
```bash
cd <repository-folder>
```

**Step 3**: Set up a virtual environment.
```bash
python3 -m venv venv
source venv/bin/activate
```

**Step 4**: Install the required libraries.
```bash
pip install -r requirements.txt
```

**Step 5**: Create a `.env` file and add your Google API key:
```bash
GOOGLE_API_KEY=your-google-api-key
```

**Step 6**: Run the Streamlit application.
```bash
streamlit run main.py
```

**Step 7**: Open the application in your browser at:
```
http://localhost:8501
```

Once the application is running, upload your PDF files through the provided interface, ask your questions, and get answers based on the documents' content.

---

Outputs:

![Screenshot 2024-09-24 170630](https://github.com/user-attachments/assets/c2f6e202-247e-4f32-a9e0-9aa6b0d28419)

![Screenshot 2024-09-24 170331](https://github.com/user-attachments/assets/61e4773b-5379-490f-8d90-59ca9ee8fdf0)

![Screenshot 2024-09-24 170501](https://github.com/user-attachments/assets/f2db1c5b-34b3-4fb4-be0b-df883e9a8a28)

![Screenshot 2024-09-24 170307](https://github.com/user-attachments/assets/bd05dd6b-bf84-4e0f-a643-2ca41d397156)
