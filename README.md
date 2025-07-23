# AI-Powered ATS Resume Checker

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.32-FF4B4B?logo=streamlit&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-blue?logo=langchain)
![Google Gemini](https://img.shields.io/badge/Google-Gemini-4285F4?logo=google&logoColor=white)

Struggling to get your resume past automated screening systems? This intelligent ATS resume checker leverages a multi-agent AI system to analyze your resume against any job description and provide actionable feedback.
This tool helps you optimize your resume by scoring it on key metrics like impact, brevity, and style, and allows you to ask specific questions about your job fit.

## ✨ Key Features

-   **Multi-Agent Analysis**: Deploys a team of specialized AI agents, each focused on a different aspect of your resume:
    -   **Impact Agent**: Scores quantifiable achievements and the use of strong action verbs.
    -   **Brevity Agent**: Identifies wordiness and redundant sections.
    -   **Style Agent**: Checks for professionalism, consistent formatting, and overall style.
    -   **Section Completeness Agent**: Ensures all essential resume sections are present.
-   **Overall ATS Score**: Calculates a final, aggregated score out of 10 to give you a clear idea of your resume's ATS-friendliness.
-   **PDF Resume Parsing**: Easily upload your resume in PDF format, and the tool will automatically extract the text content.
-   **Interactive Q&A**: Ask specific questions about your resume or how well it matches the job description, and get instant answers from an AI career advisor.
-   **User-Friendly Interface**: A clean and simple web interface built with **Streamlit**.

## 🤖 How It Works

The application uses a multi-agent approach inspired by modern AI frameworks. When you upload your resume and a job description:

1.  **Text Extraction**: The text content is extracted from your PDF resume.
2.  **Agent Invocation**: The resume text and job description are sent to four distinct AI agents, each with a specific role.
3.  **Scoring & Feedback**: Each agent analyzes the documents based on its expertise and returns a score (out of 10) along with concise feedback.
4.  **Result Aggregation**: The scores from all agents are averaged to produce a final ATS score.
5.  **Interactive Q&A**: The system keeps the context of your resume and the job description, allowing you to ask follow-up questions to a dedicated Q&A agent.

## ✍️ How to Use
1. Launch the application with `streamlit run main.py`.
2. Use the sidebar to upload your resume in PDF format.
3. Paste the target job description into the text area.
4. Click the 'Analyze Resume' button to view your scores and feedback.
5. Ask follow-up questions in the 'Resume Q&A' section.
## 🛠️ Tech Stack

-   **Web Framework**: Streamlit
-   **LLM Orchestration**: LangChain
-   **LLM Provider**: Google Generative AI (via `langchain-google-genai`)
-   **PDF Parsing**: PyPDF2
-   **Environment Management**: `python-dotenv`

## 🚀 Getting Started

Follow these steps to set up and run the project locally.

### Prerequisites

-   Python 3.9 or higher
-   A Google Gemini API Key. You can get one from [Google AI Studio](https://aistudio.google.com/app/apikey).

### 1. Clone the Repository

```sh
git clone [https://github.com/your-username/ATS-resume-tracker.git](https://github.com/your-username/ATS-resume-tracker.git)
cd ATS-resume-tracker
```

### 2. Set Up a Virtual Environment. It's recommended to use a virtual environment to manage dependencies. 
#### Create a virtual environment
```
python -m venv .venv
```
#### Activate it
```
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate
```
### 3. Install Dependencies Install the required Python packages using the pyproject.toml file. If you have uv or pip installed:
```
# Using uv (recommended)
uv pip install -r requirements.txt  # Assuming you generate a requirements.txt from pyproject.toml

# Or directly with pip
pip install -e .

(Note: Based on your pyproject.toml, you may need to adjust the install command or 
generate a requirements.txt file if one doesn't exist.)
```
### 4. Configure Environment VariablesCreate a .env file in the root directory of the project and add your Google Gemini API key:# .env
```
GEMINI_API_KEY="your_google_gemini_api_key_here"
```
### 5. Run the ApplicationOnce the setup is complete, run the Streamlit application with the following command:streamlit run main.py
```
The application will open in your default web browser.📂 Project StructureATS-resume-tracker/
├── .venv/                  # Virtual environment directory
├── .env                    # Environment variables (API key)
├── agents.py               # Defines the specialized AI agents
├── main.py                 # Main Streamlit application file
├── utils.py                # Helper functions for PDF parsing and text cleaning
├── pyproject.toml          # Project metadata and dependencies
└── README.md
```
