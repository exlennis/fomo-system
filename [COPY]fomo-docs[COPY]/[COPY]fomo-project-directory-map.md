# FOMO Project Structure (2025-03-28)

## 1. Main Project Structure
Main project folder at ~/Projects/dev/00-fomo-system/ with complete documentation and testing framework:

```
00-fomo-system/
├── docs/
│   ├── 01-planning/
│   │   ├── analysis-cli-repo-resources.md
│   │   ├── analysis-dam-*.md
│   │   ├── chat-summary-*.md
│   │   ├── claude-project-*.md
│   │   ├── research-naming-*.md
│   │   └── research-taxonomy-*.md
│   ├── 02-standards/
│   │   ├── directory-*.md
│   │   ├── fomo-controlled-VOCABULARY-*.md
│   │   ├── fomo-directory-structure-GUIDELINES-*.md
│   │   ├── fomo-naming-STANDARDS-*.md
│   │   └── fomo-tag-management-*.md
│   ├── 03-analysis/
│   │   ├── audit-apps/
│   │   │   ├── Audit-Applications-*.md
│   │   │   ├── FOMO-Audit-*.csv
│   │   │   └── File_Type_Distribution.csv
│   │   ├── audit-directory/
│   │   │   ├── directory-structure-20250124.zip
│   │   │   ├── directory-structure-20250130.zip
│   │   │   └── directory-structure-20250201/
│   │   ├── audit-noton/
│   │   │   └── screenShot_*.png
│   │   ├── audit-system-tags/
│   │   │   ├── FOMO_Tags_*.md
│   │   │   └── analysis-system-tag.md
│   │   ├── audit-warp-drive/
│   │   │   ├── 00-command-*.md
│   │   │   ├── 01-*.md
│   │   │   ├── 02-*.md
│   │   │   └── 03-*.md
│   │   ├── flow-*.png
│   │   ├── flow-*.svg
│   │   ├── fomo-directory-*.md
│   │   └── graph-*.png
│   ├── 04-implementation/
│   │   ├── approach-*.md
│   │   ├── automation-*.md
│   │   └── index-*.md
│   ├── 05-maintenance/
│   │   └── fomo-project-maintenance-log.md
│   ├── archive/
│   │   ├── *.bak.zip
│   │   ├── fomo-directory-structure-*.md
│   │   └── naming-*.md
│   ├── fomo-project-brief.md
│   ├── fomo-project-charter.md
│   ├── fomo-project-checklist.md
│   └── fomo-project-structure-20250328.md
└── tests/
    ├── report/
    │   ├── rename-log.txt
    │   ├── rename-mappings.txt
    │   ├── rename-sample-files.txt
    │   └── test-directory-snapshot.md
    ├── test-files/
    │   ├── FOMO Directory Permissions Settings.md
    │   ├── FOMO Downloads Management *.md
    │   ├── FOMO-Framework-Overview-*.md
    │   ├── FOMO-Unified Tagging System_*.md
    │   ├── FOMO_Folder_Structure_*.md
    │   ├── letter to Judy and Charge*.pages/
    │   │   ├── Contents/
    │   │   └── QuickLook/
    │   ├── markdown-*.md
    │   └── various test files and documents
    └── test-fonts/
        ├── Inter-*.otf
        ├── InterVariable-*.woff2
        ├── Roboto Mono*/*.ttf
        │   ├── noeed-RobotoMono-*.ttf
        │   └── noeed-*.ttf
        └── RobotoMonovold/
            ├── LICENSE.txt
            └── RobotoMono-*.ttf
```

## 2. Offsite Locations

### 2.1 Documentation (~/Knowledge/docs/)
Centralised location for standardised guidelines and reference documents that serve as the system-wide knowledge base for multiple projects.

```
Knowledge/docs/
├── applescript-naming-STANDARDS.md
├── chatgpt-project-GUIDELINES.md
├── font-management-GUIDELINES.md
├── font-metadata-sync-GUIDELINES.md
├── markdown-gfm-format-GUIDELINES-working.md
├── markdown-style-GUIDELINES.md
├── python-development-GUIDELINES.md
├── shell-script-naming-STANDARDS.md
├── static-fonts-naming-STANDARDS.md
├── variable-fonts-naming-STANDARDS.md
├── warp-drive-organisation-GUIDELINES.md
└── web-development-naming-STANDARDS.md
```

### 2.2 Scripts (~/System/scripts/)
Centralised location for all automation scripts and workflows that provide system-wide functionality across multiple projects.

#### 2.2.1 Key Automation Tools
- **File Management Tools**
  - `ai-batch-renamer.sh`: Intelligent file renaming using naming conventions
  - `rename-*.py`: Python-based file renaming utilities with pattern matching
  - `directory-checker.py`: Validates directory structures against standards
  - `file-renamer.py`: Advanced file renaming with metadata extraction

- **Workflow Automation**
  - `sh-warp-ai-rename`: Bundle for AI-assisted naming automation
  - `py-auto-renamer`: Python package for rule-based renaming
  - `sh-app-usage-auditor`: System usage pattern analysis tools
  - `directory-visualiser.py`: Creates visual representations of directory structures

- **Integration Tools**
  - `Mermaid`: Workflow diagrams and documentation generation
  - `WarpWorkflows`: Terminal-based automation for standard processes
  - `AppleScript`: System-level integrations for macOS applications
  - `AppleShortcut`: User-facing automation triggers

```
System/scripts/
├── AppleScript/           # AppleScript automation
│   ├── fomoRenamer.applescript
│   ├── fomoRenamerAdvanced.applescript
│   └── text*.applescript
├── AppleShortcut/         # Apple Shortcuts automation
│   ├── Fix-File-Name.shortcut
│   └── Rename-Notes-from-Content.shortcut
├── Bundle/                # Script bundles and packages
│   ├── js-font-download/
│   ├── py-auto-renamer/
│   ├── py-font-checker/
│   ├── py-font-manager/
│   ├── sh-app-usage-auditor/
│   └── sh-warp-ai-rename/
├── JavaScript/           # JS utilities and functions
│   ├── changeCase.js
│   ├── configureYargs.js
│   └── various utility scripts
├── Mermaid/             # Flow diagrams and visualizations
│   ├── flow-*.mermaid
│   ├── flow-*.svg
│   └── mermaid-viewer.html
├── Python/              # Python automation scripts
│   ├── change-case-*.py
│   ├── create-gif-from-video.py
│   └── rename-*.py
├── ShellScript/         # Shell automation scripts
│   ├── ai-batch-renamer.sh
│   ├── hazel-auto-renamer.sh
│   └── various utility scripts
└── WarpWorkflows/       # Warp terminal workflows
    ├── template/
    │   ├── warp-workflow-*.yaml
    │   └── warp-workflow-*.md
    └── working/
        └── various workflow files
```


## 3. Integration Between Project and Offsite Locations

### 3.1 Project-to-Offsite Relationships
- **Project → Documentation**: Project standards reference and build upon central standards
- **Project → Scripts**: Project tests validate and utilise centralised script functions
- **Documentation → Project**: Central guidelines inform project-specific implementations
- **Scripts → Project**: Automation tools are used for project file management tasks

### 3.2 Integration Points
- **Standard References**: Project documentation references offsite standards documents
- **Script Execution**: Project files processed by offsite automation scripts
- **Implementation Tests**: Project tests validate offsite script functionality
- **Workflow Diagrams**: Project flows visualised using offsite Mermaid templates
- **Naming Consistency**: Offsite and project files follow the same naming standards

### 3.3 Offsite References
- Documentation is externally linked in ~/Knowledge/docs/
- Scripts are externally linked in ~/System/scripts/
- Both locations follow the established naming standards

### 3.4 Version Information
- Structure last updated: 2025-04-01
- Previous version: 2025-03-28
- Changes: 
    * Updated integration with automation tools documentation
    * Enhanced cross-referencing between project and offsite resources
    * Added comprehensive documentation of automation implementations
    * Updated details on workflow analysis tools

---

*Version History:*
- v01 - 2025-03-07: Initial structure documentation
- v02 - 2025-03-28: Added explicit offsite location mapping, expanded directory structure with additional details
- v03 - 2025-04-01: Updated with automation tools integration and implementation details
