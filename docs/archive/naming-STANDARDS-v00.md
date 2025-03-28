# ==Naming Conventions (OUTDATED)==

==TO BE UPDAdATED==
==new-standard-kebab-case-hyphen.ext==

## Universal Naming Structure
This format ensures predictable sorting, efficient retrieval, and compatibility across systems. This structured naming convention ensures consistency, enforces **lowercase filenames**, maintains **underscore separators**, integrates with your existing file organisation, and is optimised for automation.

```
[category]_[subcategory]_[description]_[date]_[version]_[identifier].[extension]
```

### Component Breakdown
| Component    | Purpose                                   | Example                      |
|-------------|-------------------------------------------|----------------------------------|
| category    | High-level classification (finance, dev, design, etc.) | `invoice`, `script`, `report` |
| subcategory | Further refines classification           | `tax`, `ui_kit`, `python` |
| description | Brief summary of file content            | `logo_bosisto`, `header_nav` |
| date (YYYYMMDD) | Ensures chronological sorting       | `20250219` |
| version     | Tracks iterations (`v1`, `revA`)        | `v2.1`, `final` |
| identifier (Optional) | Unique identifier (invoice no, project ID) | `inv_2024_0156`, `ref_0032` |
| extension   | Specifies file type                      | `.pdf`, `.ai`, `.py` |

---

## Key Best Practices

### 1. **Lowercase Enforcement**
- All filenames must be **entirely lowercase** to avoid case-sensitivity issues across different operating systems (macOS, Linux, Windows).

### 2. **Underscore (_) as Separator**
- Underscores (`_`) are used as the **sole separator** for readability and compatibility with scripts, automation tools, and command-line environments.
- Hyphens (`-`) are not used to prevent confusion with flags in command-line operations.

### 3. **Date Format (YYYYMMDD)**
- All filenames must use the **ISO 8601** date format (`YYYYMMDD`) for clear chronological sorting and cross-system compatibility.

### 4. **Filename Length**
- Keep filenames **under 31 characters** for better web and cross-platform compatibility.
- Descriptions should be **concise** but **meaningful** to balance readability and practicality.

---

## Category-Specific Naming Examples

### Finance (Invoices, Tax, Payroll)
```
invoice_apple_20250219_inv_2024_0156.pdf
tax_statement_ato_20241231_tax_2024.pdf
```
**Rationale:**
- Vendor name improves searchability.
- Date-based sorting aligns with tax requirements.

---

### Design Assets (Logos, UI Kits, Templates)
```
logo_bosisto_concept_v2.ai
ui_kit_airbnb_components_v03.sketch
mockup_apple_iphone_15_v2.psd
```
**Rationale:**
- Project or brand name ensures clarity.
- Versioning prevents overwrites.

---

### Reference & Research Documents
```
guide_accessibility_wcag3_w3c_202402.pdf
report_ai_prompt_engineering_deepmind_202401.pdf
```
**Rationale:**
- Source attribution prevents confusion.
- Consistent topic-based naming aids retrieval.

---

### Code & Development
```
script_file_renamer_python_v1_2.py
function_auto_sort_js_v2.js
sql_query_finance_reports_v01.sql
```
**Rationale:**
- Language tag improves searchability.
- Versioning is critical for debugging.

---


### Screenshot
```
screenshot_[device]_[context]_[YYYYMMDD-HHMMSS].[extension]
```

| Component     | Description                                          | Example                                     |
|--------------|-------------------------------------------------------|---------------------------------------------|
| `screenshot` | Standard prefix for all screenshots                   | `screenshot`                                |
| `[device]`   | Identifier for device type (Mac, iPhone, iPad, etc.)  | `macbook`, `iphone`, `ipad`, `windows`      |
| `[context]`  | Short description of the captured content             | `safari`, `obsidian`, `activity_monitor`    |
| `[YYYYMMDD]` | Date of capture (ISO 8601 for sorting)                | `20250219`                                  |
| `[HHMMSS]`   | Time of capture (24-hour format)                      | `143522`                                    |
| `[extension]`| File format (png, jpg, etc.)                          | `.png`                                      |


**Example Renamed Files**
| Old Filename                                        | New Filename (Standardised)                        |
|-----------------------------------------------------|--------------------------------------------------|
| `Screen Shot 2015-12-10 at 6.10.42 pm.png`         | `screenshot_macbook_safari_20151210-181042.png`  |
| `3screenShot_20250203-185833_Safari.png`          | `screenshot_macbook_safari_20250203-185833.png` |
| `screenShot_Activity Monitor_2023-11-03_001364@2x.png` | `screenshot_macbook_activity_monitor_20231103-000000@2x.png` |
| `screenShot_CleanShot_2023-11-17_001466.png`      | `screenshot_macbook_cleanshot_20231117-000000.png` |
| `screenshot_FreshBooks_2023-03-15_000783.png`     | `screenshot_macbook_freshbooks_20230315-000000.png` |

*Note:* The timestamp `000000` is used if the exact time is missing.

**Why This Format?**
-  **Consistent & Predictable** – Avoids random patterns and duplicate naming.
-  **Chronologically Sorted** – Easy retrieval based on date & time.
-  **Cross-Device Compatible** – Works for macOS, iOS, Windows, and cloud storage.
-  **Automation-Friendly** – Can be easily processed with Hazel, Shortcuts, or shell scripts.
-  **Readable & Searchable** – Quickly identify device, app, and capture date.

---

### Templates & Workflows
```
template_email_newsletter_v3.docx
template_freelance_contract_v2.pdf
template_spreadsheet_budget_v1.xlsx
```
**Rationale:**
- Clearly defines the purpose of the file.
- Versioning prevents overwriting important files.

---

## Folder-Based Automation
Aligns with Smart Folders, Hazel, and Apple Shortcuts for auto-tagging and sorting.

| Folder        | Naming Pattern for Auto-Sorting |
|--------------|--------------------------------|
| `/documents/finance/` | `invoice_*`, `tax_*`, `payroll_*` |
| `/projects/dev/` | `script_*`, `sql_*`, `function_*` |
| `/design/assets/` | `logo_*`, `mockup_*`, `ui_kit_*` |
| `/research/` | `guide_*`, `report_*`, `whitepaper_*` |

---

## Implementation Strategy

1. **Start Manual Review**
   - Apply naming convention to a test batch of files.
   - Adjust based on usability before full rollout.

2. **Automate with Hazel & Apple Shortcuts**
   - Use rules to auto-rename and move files.
   - Example: Move all `invoice_*` files to `/documents/finance/`.

3. **Set Up Smart Folders for Quick Access**
   - Finder Smart Folders group files dynamically.
   - Example: One for all `*_vfinal*` design files.

4. **Implement OCR-Based Renaming for PDFs**
   - Use Apple Shortcuts or Hazel to extract text-based metadata from invoices, receipts, etc.

---

### **Automation for Renaming (Mac)**
**1. Screeshots Hazel (Recommended)**
- Create a rule to match `Screen Shot*` files.
- Use a custom renaming format:
  ```
  screenshot_macbook_%custom_text%_%date_created:YYYYMMDD-HHMMSS%.png
  ```
- Extract app name from metadata (if possible).

**2. Apple Shortcuts**
- Run a shortcut to rename new screenshots automatically.

**3. Terminal Command (Batch Rename)**
Run this command in **Terminal** to rename all screenshots in your folder:
```bash
for file in ~/Desktop/*.png; do
  timestamp=$(stat -f "%Sm" -t "%Y%m%d-%H%M%S" "$file")
  mv "$file" "screenshot_macbook_unknown_${timestamp}.png"
done
```