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

1. The Excel file is loaded into a pandas DataFrame (single source of truth)
2. User questions are converted into pandas operations by the LLM
3. The backend executes these operations safely on the dataset
4. The computed result is transformed into a clear, HR-friendly response
5. A custom chatbot UI presents the response while maintaining the provided white & purple design and Exo 2 font family

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

```
my-hrbp-agent/
│
├── app.py                 # Flask backend server
├── requirements.txt       # Python dependencies
├── HR_Dataset.xlsx        # Sample HR data
│
├── templates/
│   └── index.html        # Main chatbot UI
│
└── static/
    ├── css/
    │   └── style.css     # Custom styling
    └── js/
        └── script.js     # Frontend logic
```

---

## 🚀 How to Run the Project

### Prerequisites

- Python 3.9+
- Ollama installed: [https://ollama.com](https://ollama.com)

---

### Step 1: Clone the Repository

```bash
git clone <your-repository-link>
cd my-hrbp-agent
```

### Step 2: Create & Activate Virtual Environment

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Set Up Ollama (One-Time)

Pull the model:
```bash
ollama pull llama3
```

Start Ollama service (keep this terminal open):
```bash
ollama serve
```

### Step 5: Start the Application

Open a **new terminal**, activate the environment again, and run:

```bash
# Activate venv first
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate

python app.py
```

### Step 6: Open in Browser

Visit: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 💬 Example Questions

- "Top 5 employees with the highest loan remaining"
- "Total loan remaining across all employees"
- "Average salary by department"
- "Who has the longest tenure?"
- "List employees from Finance with active loans"
- "Show me employees who joined in 2020"
- "What is the total payroll for the IT department?"

---

## 🔒 Security & Privacy

- All data processing happens **locally** on your machine
- No data is sent to external APIs
- The Excel file remains the single source of truth
- LLM queries are processed through local Ollama instance

---

## 📝 Notes

- No paid APIs are used
- The Excel file remains the single source of truth
- The LLM is used strictly for reasoning and explanation, not data generation
- The UI follows modern design principles with accessibility in mind
- All pandas operations are executed safely with error handling

---

## 🐛 Troubleshooting

**Issue:** "Connection refused" when running the app  
**Solution:** Make sure Ollama is running (`ollama serve`)

**Issue:** LLM responses are slow  
**Solution:** This is normal for local models. Consider using a smaller model like `llama3:8b` for faster responses

**Issue:** Excel file not found  
**Solution:** Ensure `HR_Dataset.xlsx` is in the project root directory

---

## 🚀 Future Enhancements

- [ ] Add data visualization capabilities
- [ ] Support for multiple Excel files
- [ ] Export query results to CSV/PDF
- [ ] Authentication and user management
- [ ] Query history and saved searches

---

## 👤 Author

**Danyal Shah**  
Software Engineer Candidate

---

## 📄 License

This project is created as part of a technical assessment.

---

### ✅ Quick Start Checklist

- [ ] Clone the repository
- [ ] Install Ollama and pull llama3 model
- [ ] Create virtual environment
- [ ] Install dependencies (`pip install -r requirements.txt`)
- [ ] Start Ollama (`ollama serve`)
- [ ] Run the app (`python app.py`)
- [ ] Open browser at `http://127.0.0.1:5000`

---

**Made with ❤️ for intelligent HR analytics**
