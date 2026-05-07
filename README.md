LegalDoc — AI-Powered Legal Document Assistant

📄 Upload a legal document and instantly get clause simplifications, named entity extraction, document classification, and a full clause breakdown — powered by IBM Granite Guardian and Gradio.

✨ Features

- Clause Simplification — Converts complex legal language into plain English for easy understanding.
- Named Entity Recognition (NER) — Extracts parties, dates, obligations, monetary values, and key legal terms.
- Clause Extraction — Automatically identifies and lists individual clauses from the document.
- Document Type Classification — Classifies the document as an NDA, lease, employment contract, service agreement, or other type.
- Multi-format Support — Accepts PDF, DOCX, and TXT files.

🎬 Demo

Upload any legal document through the Gradio interface and receive structured analysis across five output panels in seconds.

🛠️ Tech Stack

| Component            | Technology |
| 🤖 AI Model         | [IBM Granite Guardian 3.1 2B](https://huggingface.co/ibm-granite/granite-guardian-3.1-2b) |
| 🖥️ UI Framework `   | [Gradio](https://gradio.app/) |
| 📄 PDF Parsing      | PyPDF2 |
| 📝 DOCX Parsing     | python-docx |
| ⚙️ ML Pipeline      | Hugging Face Transformers |

⚙️ How It Works

1. Text Extraction — The uploaded file is parsed based on its extension (`.pdf`, `.docx`, or `.txt`).
2. Simplification — The first 1,000 characters are sent to the Granite model with a simplification prompt.
3. NER — The first 2,000 characters are analyzed for legal entities and key terms.
4. Clause Extraction — Lines with meaningful content are split and labeled as individual clauses.
5. Classification — The document type is inferred from the first 2,000 characters.

⚠️ Limitations

- Clause simplification and NER currently use only the first 1,000–2,000 characters of a document (suitable for demos; can be extended).
- NER is prompt-based rather than fine-tuned, so results may vary by document style.
- Model inference may be slow without a GPU.
- Full-document processing with chunking for long contracts
- Risk clause flagging and compliance checks
- Downloadable structured reports (PDF/DOCX)
- Support for multilingual legal documents

👩‍💻 Author

**aiswarya-14** — [GitHub Profile](https://github.com/aiswarya-14)
