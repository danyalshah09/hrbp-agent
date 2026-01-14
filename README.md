# 🧠 My HRBP Agent

An AI-powered HR Business Partner (HRBP) chatbot that answers natural-language questions using structured HR data from an Excel file. The application uses a local LLM to reason over the dataset while ensuring all answers are computed directly from the source data.

---

## 📌 Overview

**My HRBP Agent** allows HR users to ask questions such as:

- Top employees by loan remaining  
- Total loan exposure across the organization  
- Employee join dates and tenure  
- Department-wise salary statistics  

The system ensures **accuracy and flexibility** by separating:
- **Data computation** (pandas DataFrame)
- **Language reasoning** (LLM via Ollama)

---

## 🏗️ Architecture & Approach

1. The Excel file is loaded into a pandas DataFrame (single source of truth).
2. User questions are converted into pandas operations by the LLM.
3. The backend executes these operations safely on the dataset.
4. The computed result is transformed into a clear, HR-friendly response.
5. A custom chatbot UI presents the response while maintaining the provided white & purple design and Exo 2 font family.

This hybrid approach prevents hallucinations and allows the agent to answer **any spreadsheet-related question** without relying on paid APIs.

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask  
- **Data Processing:** pandas  
- **LLM:** Llama 3 (via Ollama)  
- **Frontend:** HTML, CSS, JavaScript  
- **Styling:** Exo 2 font, white & purple theme  

---

## 📂 Project Structure

---

## 🚀 How to Run the Project

### Prerequisites
- Python 3.9+
- Ollama installed: https://ollama.com

---

### Step 1: Clone the Repository

```bash
git clone <your-repository-link>
cd my-hrbp-agent

