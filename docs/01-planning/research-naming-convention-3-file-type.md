# File Naming Conventions:  3. File Type

```java
## **Chat Summary [2025-02-06]**

### **Context**
- **Initial Query:** Best practices for naming conventions across various file types.
- **Main Topic:** Structuring file names systematically to enhance searchability, automation, and consistency.

---

### **Key Discussion Points**

#### **1. Universal Naming Convention for File Types**
- Established a **modular structure**:
  - `[Category]_[Subcategory]_[Description]_[Date]_[Identifier]_[Version].[Extension]`
  - **Example:** `Invoice_Apple_20250206_INV-2024-0156.pdf`
- **Category-Specific Rules**:
  - **Financial Docs:** `Invoice_Apple_20250206_INV-2024-0156.pdf`
  - **Design Assets:** `Logo_Adobe_2024_v01.ai`
  - **Web Dev Files:** `Script_DownloadManager_Python_v02.py`
  - **Reference Materials:** `Guide_Design-Principles_NNGroup_202401.pdf`
  - **Templates:** `Template_Email-Newsletter_v3.docx`
  
#### **2. Industry-Specific File Organisation Best Practices**
- **Design Assets:** Structured under categories like `Logos`, `Icons`, `UI Kits`, `Fonts`, and `Templates`.
- **Web Dev Projects:** Used a feature-based structure for `src`, `public`, `tests`, and `docs`.
- **Project Files:** Segregated into `Briefs`, `Research`, `Designs`, `Deliverables`.
- **Personal Finance:** Organised into `Bank Statements`, `Invoices`, `Receipts`, and `Tax Documents`.

#### **3. Date-First (`YYYYMMDD`) vs. Contextual Naming**
- **Date-First:** Used for **chronological sorting** in finance, logs, reports, and backups.
- **Hybrid Approach:** Combined date + context for **design projects and iterative work**.
  - Example: `20250206_BrandCampaign_Logo_v2.1_final.ai`
- **Automation Benefits:** Aligns with **Hazel and OCR-based renaming workflows**.

#### **4. Versioning Best Practices for Design & Development**
- **Major Changes:** `v1`, `v2`, `v3` for significant updates.
- **Minor Revisions:** `v1.1`, `v1.2` for incremental adjustments.
- **Descriptors:** `draft`, `final`, `approved`, `revA`, `revB` for clarity.
- **Example:** `20250201_AppDashboard_DarkMode_v4.0.sketch`.

#### **5. Aligning Naming with FOMO Unified Tagging**
- **Core Tags:** `#work`, `#personal`, `#reference`, `#todo`, `#archive`.
- **Smart Folders:** Automatically group files based on metadata and naming patterns.
- **Automation Integration:** Implementing Hazel, Apple Shortcuts, and Smart Folders.

#### **6. Implementation Plan & Next Steps**
- **Phase 1:** Manual file renaming for testing.
- **Phase 2:** Implement **OCR-based renaming** and Hazel automation.
- **Phase 3:** Fully integrate **Smart Folders, iCloud sync rules, and AI-powered tagging**.

---

### **Action Items**
- [ ] Refine and finalise **file type-specific naming templates**.
- [ ] Implement **OCR-based renaming automation** for PDFs.
- [ ] Test **video conversion naming conventions** before applying H.265 automation.
- [ ] Set up **Hazel rules** for auto-tagging and folder sorting.
- [ ] Establish **review checkpoints** before enabling full automation.

### **Next Steps**
Would you like:
1. Sample **Hazel or Apple Shortcuts scripts** for automation?
2. A **detailed rulebook** for handling edge cases in naming?
3. Integration guidance for **iCloud, Dropbox, and Finder Smart Folders**?
```

# **Designing a Universal Naming Convention for Specific File Types**

To create a **universal yet adaptable naming convention**, you need a structured approach that:

- **Maintains consistency** across different file types.
- **Accommodates unique naming rules** for specific categories.
- **Ensures readability and searchability** with metadata.
- **Minimises ambiguity** and maximises automation potential.

---

## **1. Core Structure**

A **modular, hierarchical structure** works best, where each file type follows a standard pattern but includes **file-type-specific components**.

### **Standard Naming Template:**

```
[Category]_[Subcategory]_[Description]_[Date]_[Identifier]_[Version].[Extension]

```

### **Components Explained:**

| Component | Purpose | Example |
| --- | --- | --- |
| **Category** | High-level grouping (e.g., Finance, Design, Code, Reference) | `Invoice`, `Receipt`, `Asset`, `Script`, `Template` |
| **Subcategory** | Further refines the file type | `Payment`, `Tax`, `Vector`, `PSD`, `UI-Kit` |
| **Description** | Contextual details for clarity | `Adobe-Logo`, `Airbnb-Brand-Guide`, `Marketing-Campaign` |
| **Date (YYYYMMDD)** | Ensures chronological sorting & easy retrieval | `20250206`, `20241201` |
| **Identifier (Optional)** | Unique project/client/reference IDs | `INV-2024-0156`, `REF-0023`, `Proj-FOMO` |
| **Version (Optional)** | Tracks edits & iterations | `v01`, `final`, `rev3` |
| **Extension** | Maintains system compatibility | `.pdf`, `.png`, `.psd`, `.py`, `.txt` |

---

## **2. File-Type-Specific Rules**

While the core structure remains the same, some **file types require additional metadata** to enhance searchability.

### **Category-Specific Naming Patterns**

### **📂 Financial Documents (Invoices, Receipts, Tax, Payroll)**

```
[Category]_[Vendor/Client]_[Date]_[Identifier].[Extension]

```

✅ **Example:**

```
Invoice_Apple_20250206_INV-2024-0156.pdf
Receipt_Amazon_20250115_TXN-827382.pdf
TaxStatement_ATO_20241231_TAX-2024.pdf

```

💡 **Why?**

- **Client/Vendor name** improves searchability.
- **Date-based sorting** aligns with tax requirements.

---

### **🎨 Design Assets (Logos, UI Kits, Templates, PSDs, Vectors)**

```
[Category]_[Brand/Project]_[Description]_[Version].[Extension]

```

✅ **Example:**

```
Logo_Adobe_2024_v01.ai
UI-Kit_Airbnb_Components_v03.sketch
Mockup_Apple-iPhone-15-v2.psd

```

💡 **Why?**

- **Project/Brand name ensures context.**
- **Versioning helps manage iterations.**

---

### **📜 Reference Materials (Research, Guides, Reports)**

```
[Category]_[Topic]_[Source]_[Date].[Extension]

```

✅ **Example:**

```
Guide_Design-Principles_NNGroup_202401.pdf
Report_Accessibility-WCAG3_W3C_202312.pdf
Research_AI-Prompt-Engineering_DeepMind_202311.pdf

```

💡 **Why?**

- **Topic-based naming helps in research.**
- **Source attribution prevents confusion.**

---

### **📜 Scripts & Code (Python, JavaScript, Shell, SQL)**

```
[Category]_[Project/Function]_[Language]_[Version].[Extension]

```

✅ **Example:**

```
Script_DownloadManager_Python_v02.py
Function_AutoRename_JS_v1.5.js
SQL_Query_InvoiceFilter_v01.sql

```

💡 **Why?**

- **Language tag aids searchability.**
- **Versioning is critical for updates.**

---

### **📝 Templates (Emails, Design, Legal Docs, Spreadsheets)**

```
[Category]_[Use-Case]_[Version].[Extension]

```

✅ **Example:**

```
Template_Email-Newsletter_v3.docx
Template_Contract-Freelance_v2.pdf
Template_Spreadsheet-Budget_v1.xlsx

```

💡 **Why?**

- **Use-case ensures clarity.**
- **Versioning prevents overwrites.**

---

## **3. Implementation Plan**

### **Step 1: Define Primary Categories**

- 🏦 **Finance** → Invoices, Receipts, Payroll
- 🎨 **Design** → Logos, UI Kits, PSDs
- 📜 **Reference** → Reports, Research, Guides
- 💻 **Code** → Python, JS, SQL scripts
- 📝 **Templates** → Emails, Contracts, Spreadsheets

### **Step 2: Automate Renaming**

- **OCR-based renaming for PDFs** (Invoices, Receipts).
- **Regex-based batch renaming** for consistent application.
- **Hazel/Automator/Raycast scripts** to auto-tag and sort.

### **Step 3: Manual Review System**

- User prefers **manual rename review before automation runs.**
- Once stable, transition to **semi-automated naming.**

---

## **Final Thoughts**

This approach **balances standardisation and flexibility** by maintaining a **consistent naming convention** while allowing **file-type-specific adaptations**. It ensures **better organisation, searchability, and automation potential** across all files.

Organizing your files effectively across various domains enhances productivity, ensures consistency, and simplifies collaboration. Below are industry-specific best practices tailored to your areas of interest:

---

### **1. Design Assets Library**

**Folder Structure:**

- **Root Folder:** Design Assets` - **Subfolders:**
    - Logos `- Icons` - UI Kits `- Fonts` - Templates `- Client Projects`**Best Practices:**
- **Consistent Naming:** se descriptive names with versioning, e.g., `Logo_CompanyName_v1.ai`.- **Metadata and Tags:** pply tags for easy searching, such as `brand`, `2025`, `vector`.- **Digital Asset Management (DAM) Tools:** onsider tools like Adobe Bridge or Eagle for visual organization and quick access.citeturn0search2

---

### **2. Web Development Project Files**

**Folder Structure:**

- **Root Folder:** ProjectName` - **Subfolders:**
    - src `- components` - styles `- assets` - public `- tests` - docs`
    **Best Practices:**
- **Modular Structure:** rganize by feature or module to enhance scalability.citeturn0search5- **Consistent Naming:** se lowercase with hyphens, e.g., `user-profile.js`.- **Version Control:** mplement Git for tracking changes and collaboration.

---

### **3. Project Files**

**Folder Structure:**

- **Root Folder:** Projects` - **Subfolders:**
    - ClientName_ProjectName `- Briefs` - Research `- Designs` - Deliverables`
    **Best Practices:**
- **Standardized Templates:** reate templates for common documents to maintain consistency.- **Regular Backups:** chedule backups to prevent data loss.- **Access Control:** et permissions to protect sensitive information.

---

### **4. Personal Finance**

**Folder Structure:**

- **Root Folder:** Personal Finance` - **Subfolders:**
    - Bank Statements `- Invoices` - Receipts `- Tax Documents`**Best Practices:**
- **Date-Based Naming:** se `YYYY

```java
Implementing effective file naming and versioning conventions is crucial for maintaining organization and ensuring efficient retrieval, especially in design projects with multiple stages and revisions.

Date-First Naming Approach:

Using a date-first format (e.g., YYYYMMDD_filename.ext) is beneficial for files that need to be sorted chronologically. This structure ensures that files are ordered by date, facilitating easy access to the most recent or specific versions. It's particularly useful for:

Daily Logs or Reports: Ensures sequential order of entries.
Meeting Minutes: Allows quick reference to specific meeting dates.
Financial Records: Organizes statements or transactions by date.
Project Progress Photos: Chronologically orders visual documentation.
By placing the date at the beginning, files naturally sort in chronological order, enhancing retrieval efficiency. 
HURIDOCS.ORG

Versioning in Design Projects:

In design projects, clear versioning is essential due to multiple stages and revisions. A consistent versioning system helps track progress and collaborate effectively. Consider the following approach:

Major Versions: Indicate significant milestones or changes (e.g., v1, v2).
Minor Revisions: Denote minor updates or tweaks (e.g., v1.1, v1.2).
Descriptors: Use clear labels like draft, final, or revA to convey the file's status.
Recommended Naming Convention:

Combine elements to create a comprehensive file name:

[ProjectName]_[AssetDescription]_[YYYYMMDD]_v[Major].[Minor]_[Status].[Extension]
Example:

BrandCampaign_LogoDesign_20250206_v2.1_final.ai
Explanation:

ProjectName: Identifies the project (e.g., BrandCampaign).
AssetDescription: Describes the asset (e.g., LogoDesign).
YYYYMMDD: Indicates the date (e.g., 20250206).
v2.1: Specifies major version 2, minor revision 1.
final: Denotes the status of the file.
.ai: File extension indicating the format.
This structured approach ensures clarity, facilitates version tracking, and enhances collaboration within design teams. 
```