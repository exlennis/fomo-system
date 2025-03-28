## File Organisation, Management & Optimisation (FOMO) Framework

### **1. Purpose & Scope**

**Project Name:** `FOMO`

**Objective:**
Develop an efficient file management system using:
1. **Tech Stack Optimisation:** Reviewing and refining current tools and apps.
2. **System Audit & Analysis:** Standardising folder structures and tagging.
3. **Sync Conflict Resolution:** Resolving iCloud/Dropbox sync conflicts and versioning issues.
4. **File System Optimisation:** Implementing automation for organisation and retrieval.
5. **Workflow & Automation Design:** Establishing mobile workflows and automation rules.
6. **Backup & Storage Strategy:** Ensuring a robust 3-2-1 backup plan for redundancy.

**Scope:**
- Prioritising Apple’s built-in tools for workflow simplicity.
- Fixing iCloud and Dropbox sync inconsistencies.
- Automating folder organisation and file management.
- Implementing mobile-friendly file access solutions.
- Configuring Time Machine and cloud backups.

**Exclusions:**
- Android/Windows workflows.
- Complex API integrations; focus on low-code/no-code automation.

---

### **2. Referenced Project Files**

```markdown
- [x] `FOMO_Framework_Overview.md` – Step-by-step project guide.
- [ ] `Tech_Stack_Audit_Report.md` – App usage evaluation.
- [ ] `Sync_Conflict_Log.md` – Resolved sync issues documentation.
- [ ] `Migration_Plan.md` – Folder structure and automation settings.
- [ ] `Mobile_Workflow_Design.pdf` – Shortcut templates for mobile workflows.
- [ ] `Backup_Strategy.pdf` – Backup implementation guidelines.
- [ ] `Change_Log.md` – Project updates tracking.
```

**Best Practices:**
- Use date-based filenames (e.g., `2024-02-15_Client_Assets.zip`).
- Compress large files for storage efficiency.

---

### **3. Tone & Writing Style**

**Tone:** Clear and supportive.
**Audience:** Graphic/Web Designers with minimal coding experience.
**Voice:** Practical, concise, and jargon-free.

**Examples:**
- *“Turn off ‘Optimise Mac Storage’ in iCloud settings to ensure all files download.”*
- *“Disable Optimize Mac Storage to resolve iCloud file locking.”*

---

### **4. Formatting & Structure**
- Use **tables** for comparisons.
- Code blocks only for necessary automation scripts.
- Australian English spelling.

| App Name   | Purpose          | Last Used   | Action  |
|------------|------------------|-------------|---------|
| Hazel      | Auto-sort files  | 2024-02-10  | Keep    |
| TagSpaces  | File tagging     | 2023-11-05  | Remove  |

---

### **5. Scope & Boundaries**

**Included:**
- Apple tools for file management.
- iCloud/Dropbox sync troubleshooting.
- Hazel-based file sorting automation.

**Not Included:**
- Android/Windows configurations.
- Custom software integrations or API setups.

---

### **6. Output Templates & Examples**

```bash
# Batch rename files by adding a date prefix:
for file in ~/Documents/*.pdf; do
  mv "$file" "$(date -r "$file" +"%Y%m%d")_$file"
done
```

```markdown
## FOMO Status
- Tech Stack Audit (15/02/2024) Completed
- Sync Fixes – 80% complete
- File Migration – Starts 20/02/2024
```

---

### **7. Workflow & Revisions**
- Update `Sync_Conflict_Log.md` after fixing issues.
- Track changes in `Change_Log.md`.
- Use pre-built Apple Shortcuts for backups.

---

### **Final Notes**
- Follow folder structures in `FOMO_Framework_Overview.md`.
- Archive old files quarterly.
- Use Apple’s built-in tools as the primary solution.
