[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![OpenAI API](https://img.shields.io/badge/OpenAI-API-blueviolet.svg)](https://beta.openai.com/)
[![Gradio](https://img.shields.io/badge/Gradio-v%3E1.0-green.svg)](https://gradio.app/)
[![Repo Size](https://img.shields.io/github/repo-size/Rishi-Kora/Agentic-AI-resume-chatbot-using-gradio)](https://github.com/Rishi-Kora/Agentic-AI-resume-chatbot-using-gradio)


# Agentic AI Resume Chatbot using Gradio

A hands-on Jupyter notebook demonstrating how to build an **agentic** AI chatbot that ingests your LinkedIn (or other) résumé as a PDF and serves it via an interactive Gradio chat interface. Powered by OpenAI’s chat completions API, this demo shows how to:

- **Parse PDF résumés** with **pypdf**  
- **Load** a custom background summary (`summary.txt`)  
- **Assemble** a system prompt that embodies your professional persona  
- **Deploy** a chat widget using **Gradio**  
- **Evaluate** responses (via a simple Pydantic evaluation model)  
- **Lay the groundwork** for a fully agentic workflow: automatic evaluation, retries, and more

---

##  Features

- **PDF ingestion**  
  Reads `me/linkedin.pdf` (replace with your own download) and extracts all text.
- **Persona summarization**  
  Loads `me/summary.txt` for a concise overview of your skills, experience, and career goals.
- **System-driven chat**  
  Crafts a multi-part system prompt so the model “plays” you—answering as if on your personal website.
- **Gradio interface**  
  One-cell launch of a web-based chat app, accessible locally at `http://127.0.0.1:7860`.
- **Evaluation scaffold**  
  Defines a simple `Evaluation` Pydantic model and evaluator prompt to judge answer quality.
- **Future roadmap**  
  Steps to add agentic capabilities—auto-evaluation, conditional retries, and end-to-end workflows.

---

##  Installation

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Rishi-Kora/Agentic-AI-resume-chatbot-using-gradio.git
   cd Agentic-AI-resume-chatbot-using-gradio


2. **Create a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install python-dotenv openai pypdf gradio pydantic
   ```

4. **Set your OpenAI API key**
   Create a file named `.env` in the project root:

   ```env
   OPENAI_API_KEY=your_api_key_here
   ```

---

##  Usage

1. **Prepare your résumé**

   * Put your LinkedIn (or other résumé) PDF at `me/linkedin.pdf`.
   * Edit `me/summary.txt` to include a short bio/overview of your background.

2. **Configure the notebook**
   In `Agentic_AI_resume_using_gradio.ipynb`, update:

   ```python
   name = "your_name_here"             # for system prompt personalization
   ```

3. **Launch the notebook**

   ```bash
   jupyter notebook Agentic_AI_resume_using_gradio.ipynb
   ```

   Run all cells. Once the Gradio app starts, visit the local URL shown in the output.

---

##  Notebook Breakdown

| Section                 | Purpose                                                      |
| ----------------------- | ------------------------------------------------------------ |
| **1. Imports & Setup**  | Load `dotenv`, OpenAI client, PDF reader, Gradio             |
| **2. Environment**      | Read API key, initialize `OpenAI()`                          |
| **3. PDF Parsing**      | Extract text from your résumé PDF                            |
| **4. Summary Loading**  | Read your custom biography from `summary.txt`                |
| **5. Prompt Assembly**  | Build a system prompt that “becomes” you                     |
| **6. Chat Function**    | Wraps OpenAI chat completions in a reusable handler          |
| **7. Gradio Launch**    | Starts an interactive chat interface                         |
| **8. Evaluation Model** | Defines `Evaluation` via Pydantic and a corresponding prompt |
| **9. Roadmap Notes**    | Sketches out next steps for full agentic workflows           |

---
## Workflow Diagram

<img width="913" height="653" alt="image" src="https://github.com/user-attachments/assets/692a7cac-9dad-4cf0-b119-0fd1c901085e" />


---

##  Contributing

Contributions, issues, and feature requests are welcome! Feel free to:

1. Fork the repository
2. Create a new feature branch
3. Submit a pull request

---

##  License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

##  Contact

**Rishi Kora**

Email: [korarishi@gmail.com](mailto:korarishi@gmail.com)

Connect with me in Linkedin: [www.linkedin.com/in/rishikora](https://www.linkedin.com/in/rishikora)

