# File Naming Conventions: 4. Automation

```markdown
## Chat Summary – Automated File Renaming with AI & Content Recognition

### **Context**
- User wants an **automated renaming system** that uses **content recognition and AI**.
- Prefers **Hazel, Apple Shortcuts, or AI-driven solutions**.
- Requires **OCR for PDFs**, **EXIF for images**, and **metadata-based file naming**.

---

### **Key Discussion Points**
#### **1. Types of Content Recognition for Automated Renaming**
- **OCR (Optical Character Recognition)**
  - Extracts text from **PDFs, scanned documents, and images**.
  - Tools: **Apple Vision, Tesseract, Google Cloud Vision**.

- **EXIF Metadata Extraction**
  - Uses **date, location, camera model** for images/videos.
  - Tools: **ExifTool, Hazel, FFmpeg, Apple Shortcuts**.

- **AI-Based Content Analysis**
  - AI models **summarise content and generate filenames**.
  - Tools: **ChatGPT (OpenAI), Claude AI, Google Vision AI**.

- **Barcode, QR Code, and Data Recognition**
  - Extracts **identifiers from invoices, receipts, and labels**.
  - Tools: **ZBar, Google Cloud Vision, Apple’s VisionKit**.

---

#### **2. Automation Workflows for File Renaming**
- **Hazel + Apple Shortcuts**
  - Hazel watches folders, Shortcuts extracts text via OCR.
  - Example: Rename PDFs based on detected text.

- **Hazel + ExifTool for Image Metadata**
  - Uses EXIF data to rename images and sort them into folders.

- **AI-Powered Renaming with ChatGPT + Hazel**
  - Extracts text, summarises, and renames documents.

- **Whisper AI for Audio Transcription-Based Renaming**
  - Uses speech-to-text AI to name recordings based on content.

---

#### **3. Best Practices for AI-Powered File Naming**
- **Concise & Descriptive Names** (e.g., `2024_Tax_Return_AUS.pdf`)
- **Standardised Date Format** (`YYYYMMDD_Filename`)
- **Avoid Special Characters** (`Meeting_Notes_2024.pdf`)
- **Use AI Confidence Scoring** (Review low-confidence OCR results before renaming)

---

### **Action Items**
- [ ] Decide on **preferred automation tools** (Hazel, Shortcuts, AI models).
- [ ] Implement **OCR-based renaming for PDFs and scanned files**.
- [ ] Set up **ExifTool automation for image renaming**.
- [ ] Test **AI-driven renaming for complex documents**.
- [ ] Determine if **manual review** should be included in the workflow.

---

### **Next Steps**
- User can choose between **rule-based, AI-driven, or hybrid automation**.
- If full automation is preferred, AI models should be **trained and validated** for accuracy.
- If needed, scripts can be provided for **Hazel, Apple Shortcuts, and AI integration**.

Would you like specific **code snippets or automation workflow templates**?

```

# **Automated File Renaming Using AI and Content Recognition**

Automating file renaming with **AI-powered content recognition** allows files to be named dynamically based on their **actual contents**, rather than just metadata or predefined rules. This enhances **searchability, organisation, and automation efficiency**. Below is a **deep dive** into the available methods, best practices, and advanced AI capabilities.

---

## **1. Types of Content Recognition for Automated Renaming**

### **A. Text Extraction (OCR for PDFs, Scans, and Images)**

OCR (Optical Character Recognition) allows files to be renamed based on detected text content.

- **Use Cases**:
    - Extract invoice numbers from **PDF receipts** to rename files (`Invoice_20240206.pdf`).
    - Identify the **title of a scanned document** and use it for renaming.
    - Recognise handwritten or printed text in images (e.g., **scanned notes, book covers**).
- **Tools**:
    - **Apple Vision Framework** *(macOS/iOS native OCR – used by Hazel, Shortcuts)*
    - **Tesseract OCR** *(Open-source, supports multiple languages and handwriting)*
    - **Google Cloud Vision OCR** *(AI-powered cloud-based OCR)*
    - **Adobe Acrobat Pro** *(Built-in OCR with metadata extraction)*

### **B. Metadata Extraction (EXIF for Images, Video Metadata, PDF Properties)**

- **Use Cases**:
    - Rename **photos** using **date, GPS location, and camera model**.
        - `IMG_20240206_Melbourne_Daytime.jpg`
    - Rename **videos** based on resolution, duration, and encoding type.
        - `Video_4K_HDR_120fps.mp4`
    - Extract **PDF properties** (title, author, keywords) and use them for naming.
        - `ResearchPaper_Author_2024.pdf`
- **Tools**:
    - **ExifTool** *(Extracts metadata from images, PDFs, audio, and video files)*
    - **Hazel** *(Reads metadata from files and renames them accordingly)*
    - **Apple Shortcuts** *(Can extract image/video metadata using built-in actions)*
    - **FFmpeg** *(Can extract video/audio metadata and rename files based on it)*

### **C. AI-Based Content Analysis (LLM, NLP, and Machine Learning)**

AI models can go beyond simple metadata and extract **contextual meaning** from files.

- **Use Cases**:
    - **Summarise document content** and rename files based on their key topics.
        - `MeetingNotes_AppleVisionStrategy.pdf`
    - Use **speech-to-text AI** to rename **audio recordings and podcasts**.
        - `Interview_TimCook_2024.m4a`
    - Categorise **news articles, blog posts, or research papers** based on AI-driven topic analysis.
        - `AIRegulation_WhitePaper_2024.pdf`
- **Tools**:
    - **ChatGPT/OpenAI API** *(Summarises documents, extracts key phrases)*
    - **Whisper AI (OpenAI)** *(Speech-to-text model for transcribing audio)*
    - **Claude AI (Anthropic)** *(Understanding context and summarising content)*
    - **Google Vision AI** *(Classifies images, reads text, and extracts features)*

### **D. Barcode, QR Code, and Data Recognition**

- **Use Cases**:
    - Rename **invoices or shipping labels** using barcode data.
    - Extract **product details** from QR codes for consistent naming.
    - Automate renaming of scanned documents based on **barcode identifiers**.
- **Tools**:
    - **ZBar (CLI tool for barcode recognition)**
    - **Google Cloud Vision API (QR/Barcode detection)**
    - **Apple’s VisionKit (Native barcode scanning on iOS/macOS)**

---

## **2. Automation Workflows for File Renaming**

### **Workflow 1: Hazel + Apple Shortcuts**

💡 **Best for:** Local automation, OCR-based PDF renaming, image EXIF metadata-based renaming.

1. **Hazel watches a folder (e.g., ~/Downloads/)**
2. **Apple Shortcuts extracts text from PDFs/images using OCR.**
3. **Hazel renames the file based on extracted text.**
4. **Moves renamed file to an appropriate folder.**

### **Workflow 2: Hazel + ExifTool for Image Metadata**

💡 **Best for:** Photos, videos, and scanned images using EXIF metadata.

1. **Hazel detects a new image file.**
2. **ExifTool extracts GPS location, timestamp, and camera model.**
3. **Hazel renames the file (`2024-02-06_Melbourne_Sunset.jpg`).**
4. **Moves it to a structured folder (`Photos/2024/February`).**

### **Workflow 3: AI-Powered Renaming with ChatGPT + Hazel**

💡 **Best for:** AI-based naming using document content, LLM processing, and NLP.

1. **Hazel detects a new document (PDF, text file, or report).**
2. **Apple Shortcuts extracts text and sends it to an OpenAI GPT model.**
3. **GPT suggests a meaningful filename based on the document’s content.**
4. **Hazel renames the file and moves it to the correct folder.**

### **Workflow 4: Whisper AI for Audio Transcription-Based Renaming**

💡 **Best for:** Naming voice memos, interviews, and podcasts.

1. **New audio file added to `~/Recordings/`.**
2. **Whisper AI transcribes the first 10 seconds.**
3. **Hazel renames file based on detected keywords.**
    - `2024_Interview_AppleVision.m4a`
4. **File is sorted into `~/Audio/Interviews/`.**

---

## **3. AI-Powered File Naming Best Practices**

To maintain **consistency and accuracy**, apply best practices for AI-driven file renaming:

1. **Keep filenames concise but descriptive.**
    - ❌ `Document_482038320832.pdf`
    - ✅ `2024_Tax_Return_AUS.pdf`
2. **Standardise date formatting.**
    - ✅ Use `YYYYMMDD` to maintain chronological order (`20240206_Invoice.pdf`).
3. **Avoid special characters** that may break compatibility.
    - ❌ `Meeting: Notes?!.pdf`
    - ✅ `Meeting_Notes_2024.pdf`
4. **For OCR-based naming, always verify text accuracy manually first.**
    - AI-driven renaming should be **reviewed manually** before full automation.
5. **Use AI confidence scoring for automation decisions.**
    - If OCR accuracy < 90%, **prompt for manual review** instead of renaming.

---

## **4. Tools Comparison for Automated File Renaming**

| Feature | Hazel 5 | Apple Shortcuts | ExifTool | OpenAI GPT | Whisper AI |
| --- | --- | --- | --- | --- | --- |
| **OCR Text Extraction** | ✅ Yes | ✅ Yes | ❌ No | ✅ Yes | ❌ No |
| **EXIF Metadata Support** | ✅ Yes | ✅ Limited | ✅ Full | ❌ No | ❌ No |
| **AI-Powered Naming** | ❌ No | ❌ No | ❌ No | ✅ Yes | ✅ Yes |
| **Audio Transcription** | ❌ No | ❌ No | ❌ No | ✅ Yes | ✅ Yes |
| **Manual Review Step** | ✅ Yes | ✅ Yes | ❌ No | ✅ Yes | ✅ Yes |

---

## **Final Recommendation**

For your **file automation and renaming needs**, a **multi-step hybrid workflow** is ideal:

1. **Use Hazel for rule-based automation.**
2. **Integrate Apple Shortcuts for OCR text extraction (for PDFs, receipts, and scanned documents).**
3. **Incorporate AI models (ChatGPT/Whisper AI) for document summaries and intelligent renaming.**
4. **Use ExifTool for media metadata-based renaming (images, videos, audio).**

Would you like help setting up **scripts for these workflows**, or do you need guidance on **integrating AI APIs for renaming automation?**