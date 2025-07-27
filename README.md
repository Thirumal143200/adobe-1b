# Adobe Hackathon 2025 - Round 2 Challenge 1b: Multi-Collection PDF Table Extractor

This project is a solution for the Adobe India Hackathon 2025 - Round 2 Challenge 1b.  
It processes multiple collections of PDFs, extracts tabular data from each file, and compiles the results into a single output.json.

---

## 📁 Project Structure

```bash
adobe-hackathon-round1b/
├── collections/
│   ├── sample1/
│   │   ├── sample3.pdf
│   │   ├── sample5.pdf
│   │   ├── sample7.pdf
│   │   ├── sample9.pdf
│   │   └── sample11.pdf
│   ├── sample2/
│   │   ├── sample4.pdf
│   │   ├── sample6.pdf
│   │   ├── sample8.pdf
│   │   ├── sample10.pdf
│   │   └── sample12.pdf
│   └── input.json
├── output/
│   └── output.json
├── extractor/
│   └── extract_tables.py
└── README.md
---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/adobe-hackathon-round1b.git
cd adobe-hackathon-round1b

2. Install Dependencies

pip install -r requirements.txt

3. Run Table Extraction

To extract tables from a single PDF:

python extractor/extract_tables.py collections/sample1/sample3.pdf

To process all PDFs in all collections using input.json:

# Automatically called in evaluation or demo environment


---

🧠 How It Works

Each collection (e.g., sample1, sample2) contains multiple PDFs.

The extract_tables.py script uses PDF table detection techniques (e.g., pdfplumber, pdfminer, etc.) to extract tables.

The extracted tables are stored in structured JSON format in output/output.json.



---

📝 Sample Input (input.json)

{
  "collections": [
    {
      "name": "sample1",
      "files": [
        "sample3.pdf", "sample5.pdf", "sample7.pdf", "sample9.pdf", "sample11.pdf"
      ]
    },
    {
      "name": "sample2",
      "files": [
        "sample4.pdf", "sample6.pdf", "sample8.pdf", "sample10.pdf", "sample12.pdf"
      ]
    }
  ]
}


---

📦 Output Format (output.json)

The output JSON contains extracted tables structured by collection and PDF filename:

{
  "sample1": {
    "sample3.pdf": {
      "tables": [
        { "page": 1, "table": [ [...], [...] ] },
        ...
      ]
    },
    ...
  },
  ...
}


---

🧪 Tested On

Python 3.10

Windows 10 / 11

VS Code with venv



---

🔗 Credits

Developed by [Your Name] for Adobe India Hackathon 2025
Inspired by official Adobe Challenge 1B demo and spec.