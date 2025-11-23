# PDF Summarizer & Quiz Generator Agent

This project implements a PDF Summarizer and Quiz Generator Agent using the OpenAgents SDK, Chainlit for the web interface, and PyPDF for PDF text extraction. The agent utilizes the Gemini 2.5 Flash model for summarization and quiz generation.

## 🚀 Getting Started

Follow these steps to set up and run the application.

### 1. Project Structure

The project has the following structure:

```
project/
├── .env                 # API keys (GEMINI_API_KEY)
├── agent.py            # Agent configuration & tool setup
├── utils.py            # PDF text extraction helper
├── app.py              # Chainlit UI and event handlers
├── pyproject.toml      # Dependencies
└── README.md           # This file
```

### 2. Environment Setup

Make sure you have `uv` installed. If not, you can install it using `pip`:
```bash
pip install uv
```

Navigate to the `project` directory and install the dependencies:
```bash
cd project
uv sync
```

### 3. Configuration

#### `.env`

Create a `.env` file in the `project` directory and add your Gemini API key:

```
GEMINI_API_KEY=your_actual_api_key_here
```
**Important:** Replace `your_actual_api_key_here` with your actual Gemini API key.

### 4. Running the Application

Navigate to the `project` directory and run the Chainlit application:

```bash
cd project
chainlit run app.py -w
```

The `-w` flag enables auto-reloading when code changes are detected.

## 📝 Usage

1.  **Upload a PDF:** Once the Chainlit UI is open in your browser, you will be prompted to upload a PDF file.
2.  **Get Summary:** The agent will process the PDF, extract its text, and provide a summary of the content.
3.  **Generate Quiz:** After the summary, you will be given an option to "Create Quiz". Click the button or type "Create Quiz" in the chat to generate a multiple-choice quiz based on the original PDF content.

## 🎓 Success Criteria

-   A non-technical user can upload a PDF and get a summary.
-   The quiz accurately reflects PDF content.
-   All responses stream smoothly.
-   Code follows the zero-bloat protocol.

---
