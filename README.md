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


git clone <your-repository-link>
cd my-hrbp-agent

### Step 2: Create & Activate Virtual Environment
python -m venv venv
venv\Scripts\activate

### Step 3: Install Dependencies
pip install -r requirements.txt

### Step 4: Set Up Ollama (One-Time)

Pull the model:

ollama pull llama3


Run Ollama (keep this terminal open):

ollama run llama3

### Step 5: Start the Application

Open a new terminal, activate the environment again, and run:

python app.py

### Step 6: Open in Browser

Visit:

http://127.0.0.1:5000

💬 Example Questions

“Top 5 employees with the highest loan remaining”

“Total loan remaining across all employees”

“Average salary by department”

“Who has the longest tenure?”

“List employees from Finance with active loans”

📝 Notes

No paid APIs are used.

The Excel file remains the single source of truth.

The LLM is used strictly for reasoning and explanation.

The UI follows the reference screenshots provided in the task.

👤 Author

[Your Name]
Software Engineer Candidate


---

### ✅ What to do now (IMPORTANT)

1. Paste this into `README.md`
2. Replace:
   - `<your-repository-link>`
   - `[Your Name]`
3. Commit & push

```bash
git add README.md
git commit -m "Add project README"
git push
