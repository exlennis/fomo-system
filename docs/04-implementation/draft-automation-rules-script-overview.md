# FOMO Automation Rules & Script Overview

This document lists all the automation rules and components found in the FOMO system project documentation.


---

List of Automation to set up
Would you like an automation shortcut to help tag new notes faster?
Would you like an automation shortcut to quickly tag notes while you transition?
Would you like a Shortcut automation to quickly apply tags when moving notes?
Would you like an automation shortcut to check for inconsistent tag casing and suggest fixes?
automation for Retrieve all notes and extract tags.
automation for Check for variations (e.g., #Work, #work, #WORK).
automation for Suggest a unified format (e.g., #work).
automation for Provide a list of notes needing updates so you can manually confirm before applying changes.


  


📌📌📌📌
- file extension consistency, change old standards to new ones, e.g. .markdown to .md, .jpeg vs .jpg???
- an automation shortcut to check for inconsistent in tag casing and suggest fixes e.g. work vs working vs Work
- an automation shortcut to check for inconsistent in file naming and suggest fixes . e.g. _ vs -
- Auoamte app update workflow > Latest installation then check macudpater and app store ? brew instlls?
- auto cover files: with a dropzone setup-
- .doc or .docs to .md


  


WORKFLOWS

AI-powered content analysis to:
1️⃣ Scan note content and extract key topics, themes, and keywords.
2️⃣ Recommend connections between notes based on shared concepts.
3️⃣ Identify redundant or overlapping notes for better organisation.





```
Yes! You can **automatically convert** `.doc` or `.docx` files to `.md` (Markdown) using **Pandoc**, Python, or Google Apps Script. Below are three methods to automate this process.

---

## **Method 1: Pandoc (Best for Batch Conversion)**
**Pandoc** is the most powerful tool for document conversion.

### **Setup Pandoc**
1. **Install Pandoc**:
   - **macOS (Homebrew)**:
     ```sh
     brew install pandoc
     ```
   - **Windows (Chocolatey)**:
     ```sh
     choco install pandoc
     ```
   - **Linux**:
     ```sh
     sudo apt install pandoc
     ```

2. **Convert a Single File**
   ```sh
   pandoc input.docx -t markdown -o output.md
   ```

3. **Batch Convert All `.docx` in a Folder**
   ```sh
   for file in *.docx; do pandoc "$file" -t markdown -o "${file%.docx}.md"; done
   ```

4. **Automate with a Scheduled Script**
   Create a cron job (Linux/macOS) or a scheduled task (Windows) to run the script automatically.

---

## **Method 2: Python + Pandoc (For More Control)**
Use **Python with Pandoc** to automate batch conversion.

### **Install Dependencies**
```sh
pip install pypandoc
```

### **Python Script**
```python
import os
import pypandoc

input_folder = "path/to/docx/files"
output_folder = "path/to/md/output"

for filename in os.listdir(input_folder):
    if filename.endswith(".docx") or filename.endswith(".doc"):
        input_path = os.path.join(input_folder, filename)
        output_path = os.path.join(output_folder, filename.rsplit(".", 1)[0] + ".md")

        pypandoc.convert_file(input_path, 'md', outputfile=output_path)
        print(f"Converted: {filename} → {output_path}")
```

### **Automate the Script**
- **macOS/Linux**: Add to `crontab -e`
  ```sh
  0 * * * * /usr/bin/python3 /path/to/script.py
  ```
- **Windows**: Use Task Scheduler.



---

## Planned Automation Components

1. **fomo-project-charter-v01.md**:
   - Project Approach Section
     - Line 55: Hazel Rule: Automation-First Mindset - Prioritise automated solutions using Hazel, Shortcuts, Python, and n8n
     - Line 56: Integration Rule: Human-Agent Collaboration - Leverage Claude's capabilities alongside human expertise
   - Project Organization Section
     - Line 69: Implementation Rule: Implementation-and-Automation - Develops scripts, Hazel rules, and technical solutions
     - Line 78: Documentation Rule: FOMO-Automation-Scripts-v01.md - Technical solutions for file management
   - Project Scope Section
     - Line 97: Hazel Rule: Hazel rule sets for automated file organisation
     - Line 98: Apple Shortcuts Rule: Apple Shortcuts for streamlined processing
     - Line 99: Python Script Rule: Python scripts for specialised operations
     - Line 100: n8n Rule: n8n workflows for integrated processes
     - Line 104: Automation Rule: Automated file naming and processing
   - Success Criteria Section
     - Line 120: Performance Rule: Automation Coverage - 80% of routine tasks

2. **fomo-project-setup-plan-v01.md**:
   - Guiding Principles Section
     - Line 45: Automation Rule: Prioritise Automation - Automate processes wherever possible using tools like Hazel, Shortcuts, Python scripts, and n8n workflows
   - Roles and Responsibilities Section
     - Line 71-73: Implementation Rule: Implementation-and-Automation - Focuses on practical scripts and workflows, Contains automation rules for Hazel, Shortcuts, etc.
   - Document Framework Section
     - Line 110-115: Documentation Rule: Automation-Scripts-v01.md - Collection of scripts for batch renaming, Hazel rules for automatic organisation, Apple Shortcuts for common file handling tasks, Python scripts for specialised operations
   - Automation Approach Section
     - Line 226-231: Hazel Rule: Hazel Configuration - Create rule sets for different folders, Define pattern matching for file types, Establish naming transformations, apply naming conventions to screenshots, Set up sorting rules, Move files to appropriate directories based on type
     - Line 232-237: Apple Shortcuts Rule: Apple Shortcuts - Quick renaming of selected files, Capture and process screenshots, Standardise naming on save dialogs, Build file processing workflows
     - Line 238-242: Script Rule: Scripts (Python, AppleScript and other) - Batch rename based on conventions, Analyse compliance with standards, Generate reports on system organisation
     - Line 243-247: n8n Rule: n8n Workflows - Automate file processing for cloud services, Monitor and organise shared files, Integrate with other services
     - Line 248-254: Prioritization Rule: Automation Priorities - Screenshots and Downloads folder, High-volume file creation processes, Document save templates, Batch processing for existing files, Monitoring and reporting
   - Performance Metrics Section
     - Line 329-332: Performance Rule: Automation Coverage - Automate 80% of routine file management tasks

3. **fomo-claude-system-instructions-v02.md**:
   - Learning Objectives Section
     - Line 210-214: Skill Development Rule: Automation Skill Development - Build expertise in Hazel rule creation, Develop Apple Shortcuts proficiency, Enhance Python scripting capabilities, Explore n8n workflow potential
   - System Updates Section
     - Line 188-191: Maintenance Rule: System Updates - Process for updating automation rules, Procedure for revising standards, Method for implementing new features, Path for resolving issues

4. **reserach-file-automation-system-grok.md**:
   - Hazel Automation Section
     - Line 34-39: Hazel Rule: File Renaming - Standardise downloaded PDFs, rename to "YYYY-MM-DD_Document.pdf"
     - Line 41-45: Hazel Rule: File Sorting - Sort images to a Pictures folder
     - Line 47-51: Hazel Rule: Image Optimisation - Compress new images and tag with "Optimised"
     - Line 88-93: Hazel Rule: Hazel Automation for Tagging - Add tag "Document" to PDFs
     - Line 191: Hazel Rule: Apply naming conventions via Hazel renaming rules
   - AppleScript Section
     - Line 56-67: AppleScript Rule: Example Script for compressing images in a folder
   - Integration Section
     - Line 123-131: Integration Rule: Raycast Integration Custom Scripts - Example Script to open a Smart Folder
   - AI Implementation Section
   - AI Implementation Section
     - Line 141-150: AI Rule: AI Automation Exploration - Automatic Tagging using Apple's Vision framework, Content Analysis with HoudahSpot

5. **fomo-naming-standards-v01.md**:
   - Implementation Guidelines Section
     - Line 213: Hazel Rule: Configure Hazel rules to automatically rename files based on naming standards
     - Line 214: Shortcuts Rule: Create Shortcuts for streamlined naming during save operations
     - Line 215: Python Script Rule: Develop Python scripts for batch processing and compliance checking
     - Line 216: n8n Rule: Set up n8n workflows for integrated file processing
   - Version Control Integration Section
     - Line 220: Git Rule: Configure git hooks to validate file names before commit
   - Success Measures Section
     - Line 311: Automation Success Rule: 80% of routine file naming handled automatically
   - Benefits Section
     - Line 20: Automation Principle: Enable effective automation through predictable patterns

## Planned Automation Overview
| # | Hazel Rules | Apple Shortcuts | Python Scripts | AppleScript | n8n Workflows | Git Automation |
|---|-------------|-----------------|----------------|-------------|---------------|--------------|
| 1 | PDF Standardization | Quick Renaming | Batch Renaming | Image Compression | Cloud Processing | Filename Validator |
| 2 | Image Sorting | Screenshot Processor | Compliance Checker | Hazel Extender | File Monitor | |
| 3 | Image Compression | Save Dialog Helper | Organization Reporter | Custom Processor | Service Integrator | |
| 4 | Auto Tagging | File Workflow | File Analyzer | | | |
| 5 | Type-Based Filing | AI Vision Tagger | | | | |
| 6 | Pattern Matcher | | | | | |
| 7 | File Renamer | Save Template | | | | |

## Implementation Status

The FOMO system project is currently in its planning phase. While detailed documentation exists outlining planned automation components, implementation scripts have not yet been developed. The scripts directory exists but does not currently contain complete automation implementation files.

## Learning Objectives

Through implementing these automation components, the project aims to:

- Build expertise in Hazel rule creation
- Develop Apple Shortcuts proficiency
- Enhance Python scripting capabilities
- Explore n8n workflow potential
- Integrate with version control systems through git hooks


## Resources

https://github.com/matthewrenze/rename-images
https://github.com/jdmonaco/pdf-title-rename
https://github.com/ronakg/smart-image-renamer
https://github.com/chrissimpkins/fontname.py