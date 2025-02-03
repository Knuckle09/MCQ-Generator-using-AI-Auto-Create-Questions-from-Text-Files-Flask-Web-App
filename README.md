**MCQ Generator using AI Auto Create Questions** 

**Demo Images**
![image](https://github.com/user-attachments/assets/1a111142-bfd0-49fb-b14f-217d21c52e5b)
### **Project Overview: MCQ Generator Web App**  

#### **1. Purpose:**  
- A **Flask-based web application** that generates **Multiple-Choice Questions (MCQs)** from uploaded text-based files.  

#### **2. Technologies Used:**  
- **Backend:** Flask (Python web framework)  
- **File Handling:** pdfplumber, docx, csv, werkzeug.utils  
- **AI Model:** Google Gemini (via `google.generativeai`)  
- **PDF Generation:** fpdf  
- **Frontend:** HTML templates (`index.html`, `results.html`)  

#### **3. Features & Functionality:**  
✅ **File Upload:** Users can upload PDF, TXT, or DOCX files.  
✅ **Text Extraction:** The app extracts text content from the uploaded file.  
✅ **AI-Powered MCQ Generation:** Uses Google Gemini API to generate MCQs based on extracted text.  
✅ **MCQ Output Format:** Each MCQ includes:  
   - Question  
   - Four answer choices (A, B, C, D)  
   - Correct answer indication  
✅ **Download Options:** Users can download MCQs in **TXT or PDF format**.  

#### **4. Workflow:**  
1️⃣ **Upload a File** → 2️⃣ **Extract Text** → 3️⃣ **Generate MCQs (via AI)** → 4️⃣ **Save & Display Results** → 5️⃣ **Download MCQs as TXT/PDF**  

#### **5. Flask Routes:**  
- **`/`** → Renders the file upload page.  
- **`/generate`** → Handles file upload, text extraction, MCQ generation, and result display.  
- **`/download/<filename>`** → Allows downloading of generated MCQs.  

#### **6. File & Folder Structure:**  
- `uploads/` → Stores uploaded files.  
- `results/` → Stores generated MCQs in TXT/PDF format.  

#### **7. Error Handling & Security:**  
- **Allowed File Types:** Only PDF, DOCX, TXT files are processed.  
- **File Security:** Uses `secure_filename` to prevent malicious uploads.  
- **Folder Management:** Automatically creates `uploads/` and `results/` if they don’t exist.  

#### **8. Deployment Considerations:**  
- Can be hosted on **Heroku, AWS, or any Flask-compatible server**.  
- Needs **Google Gemini API Key** for MCQ generation.  
