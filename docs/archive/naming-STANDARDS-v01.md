# FOMO Naming Standards v01

## 1. Introduction and Purpose

### 1.1 Purpose
This document establishes the file naming conventions for the File Organisation, Management & Optimisation (FOMO) project. It provides a comprehensive framework to ensure files are named consistently, meaningfully, and in a way that balances human readability with machine processing requirements.

### 1.2 Scope
These naming standards apply to:
- Design projects and assets
- Development projects and code
- Personal files (documents, screenshots, invoices)
- Special collections (fonts, design assets, reference materials)
- System and configuration files

### 1.3 Benefits
Implementing these standards will:
- Reduce time spent searching for files
- Minimise cognitive load when saving or organising files
- Enable effective automation through predictable patterns
- Ensure consistent organisation across projects
- Facilitate cross-platform compatibility
- Support both manual and AI-assisted file management

## 2. Core Principles

### 2.1 Clarity
Names should immediately convey content and purpose without requiring the file to be opened.

### 2.2 Consistency
Similar files should follow identical naming patterns for predictability.

### 2.3 Brevity
Balance descriptiveness with concise expressions; avoid unnecessary redundancy.

### 2.4 Human-Scannable
Names should be easily readable by humans, with natural word breaks and logical ordering.

### 2.5 Machine-Readable
Names should facilitate automated processing, searching, and sorting.

### 2.6 Contextual Adaptability
While maintaining system-wide consistency, accommodate domain-specific needs where appropriate.

## 3. Technical Specifications

### 3.1 Case Format
The primary naming convention is kebab-case:
- All lowercase letters
- Words separated by hyphens
- No spaces or underscores
- No special characters except hyphens and periods (for specific uses)

Examples:
```
project-report.pdf
meeting-notes-client.md
hero-image-homepage.jpg
```

### 3.2 Date Format
Use ISO 8601 format (YYYYMMDD) without separators:
- Four-digit year
- Two-digit month (with leading zero if needed)
- Two-digit day (with leading zero if needed)
- Place date after the descriptive portion of the name

Examples:
```
meeting-minutes-20250301.md
project-proposal-202502.pdf
annual-report-2025.docx
```

### 3.3 Version Numbering
Use v## format with leading zeros:
- Prefix with "v"
- Two-digit number with leading zero for numbers under 10
- Place version number at the end of the name, before the extension

Examples:
```
logo-design-v01.svg
presentation-client-v02.pptx
application-config-v10.json
```

### 3.4 Special Character Policy
- **Prohibited characters**: `!@#$%^&*()=+[]{};:'"\|,/<>?` and spaces
- **Allowed characters**: 
  - Hyphens (-) for word separation
  - Periods (.) for file extensions and specific uses (e.g., language codes)
  - Underscores (_) only for specific cases like pixel density indicators

## 4. Naming Patterns by File Type

### 4.1 Documents and Reports
Pattern: `[project]-[type]-[descriptor]-[YYYYMMDD]-v[##].[ext]`

Examples:
```
fomo-report-quarterly-20250301-v02.pdf
client-brief-website-redesign-20250215-v01.docx
project-proposal-mobile-app-202503-v03.md
```

### 4.2 Meeting Notes and Communications
Pattern: `[meeting-type]-[context]-[YYYYMMDD].[ext]`

Examples:
```
meeting-kickoff-20250310.md
call-client-feedback-20250322.md
workshop-ux-planning-20250405.md
```

### 4.3 Screenshots and Captures
Pattern: `screenshot-[device]-[context]-[YYYYMMDD]-[HHMMSS].[ext]`

Examples:
```
screenshot-macbook-safari-20250301-143022.png
screenshot-iphone-app-checkout-20250302-091545.jpg
```

### 4.4 Design Assets
Pattern: `[project]-[asset-type]-[descriptor]-v[##].[ext]`

Examples:
```
fomo-logo-dark-v03.svg
client-banner-homepage-v01.jpg
project-icon-download-v02.png
```

### 4.5 Code and Development Files
Pattern: `[function/purpose]-[language].[ext]` or follow language conventions

Examples:
```
file-renamer.py
api-client.js
UserProfile.tsx  # React component using PascalCase
```

### 4.6 Configuration Files
Follow standard naming conventions for the platform or maintain established names

Examples:
```
.env-production
.env-development
docker-compose.yml
tsconfig.json
```

## 5. Special Cases and Exceptions

### 5.1 Multilingual Files
For files available in multiple languages, add the ISO 639-1 language code before the extension:

Examples:
```
user-guide.en.pdf
user-guide.fr.pdf
product-description.en-au.md
```

### 5.2 Temporary Files
Prefix with `tmp-` and include date to facilitate cleanup:

Examples:
```
tmp-export-data-20250315.csv
tmp-image-processing-20250310.png
```

### 5.3 Framework-Specific Files
When working within frameworks with established conventions, follow the framework's standards:

Examples:
```
# React components (PascalCase)
ButtonGroup.tsx
UserProfile.js

# Python modules (snake_case)
database_connector.py
```

### 5.4 Pixel Density Indicators
For images with different pixel densities, use an underscore followed by the density:

Examples:
```
icon-menu_2x.png
logo-small_3x.png
```

## 6. Implementation Guidelines

### 6.1 New Files
- Apply these naming conventions to all new files immediately
- Configure save dialogs and templates to default to these patterns
- Use automation tools to enforce naming on file creation

### 6.2 Existing Files
- Prioritise renaming active project files
- Use batch renaming tools for bulk updates
- Address high-value historical content as resources permit

### 6.3 Automation Tools
- Configure Hazel rules to automatically rename files based on these standards
- Create Shortcuts for streamlined naming during save operations
- Develop Python scripts for batch processing and compliance checking
- Set up n8n workflows for integrated file processing

### 6.4 Version Control Integration
- Ensure naming conventions align with version control best practices
- Configure git hooks to validate file names before commit
- Document any special considerations for repository organisation

## 7. Examples and Templates

### 7.1 Design Project Example
```
client-project/
├── briefs/
│   ├── client-brief-initial-20250301-v01.pdf
│   └── client-brief-revised-20250315-v02.pdf
├── design/
│   ├── client-wireframes-homepage-v01.sketch
│   ├── client-wireframes-homepage-v02.sketch
│   ├── client-mockup-homepage-v01.psd
│   └── client-style-guide-v01.pdf
└── assets/
    ├── client-logo-primary-v01.svg
    ├── client-logo-secondary-v01.svg
    ├── client-hero-homepage-v01.jpg
    └── client-icon-set-v01.ai
```

### 7.2 Development Project Example
```
app-project/
├── src/
│   ├── components/
│   │   ├── Button.tsx
│   │   └── UserProfile.tsx
│   ├── utils/
│   │   ├── date-formatter.js
│   │   └── api-client.js
│   └── styles/
│       └── global-styles.css
├── docs/
│   ├── api-documentation-20250301.md
│   └── setup-guide-20250301.md
└── config/
    ├── .env-development
    └── .env-production
```

### 7.3 Personal Files Example
```
personal/
├── invoices/
│   ├── invoice-client-20250301-001.pdf
│   └── invoice-client-20250315-002.pdf
├── documents/
│   ├── contract-freelance-20250201.pdf
│   └── agreement-nda-client-20250301.pdf
└── screenshots/
    ├── screenshot-macbook-design-feedback-20250305-143022.png
    └── screenshot-iphone-app-testing-20250310-091545.jpg
```

## 8. Maintenance and Governance

### 8.1 Regular Audits
- Conduct monthly checks of recently created files
- Use automated tools to measure compliance
- Review naming patterns for effectiveness and usability

### 8.2 Updates and Revisions
- Document challenges and solutions in the Maintenance Log
- Refine standards based on practical experience
- Version this document for significant changes

### 8.3 Exceptions Management
- Document necessary exceptions in the Special Cases document
- Maintain a registry of approved variations
- Review exceptions periodically for patterns that might indicate needed changes

## 9. Integration with Other FOMO Documents

This Naming Standards document works in conjunction with other FOMO project documents:

- **Directory-Structure-v01.md**: Defines the folder hierarchy these named files will live within
- **Implementation-Plan-v01.md**: Outlines the phased approach to implementing these standards
- **Automation-Scripts-v01.md**: Contains scripts and tools to enforce these naming conventions
- **Special-Cases-v01.md**: Provides detailed guidance for exceptions to these standards
- **Naming-Cheatsheet-v01.md**: Quick reference guide for daily application

## 10. Success Measures

The effectiveness of these naming standards will be measured by:

- **File Location Time**: 50% reduction in time to locate specific files
- **Naming Compliance**: 95% of new files following conventions
- **Cognitive Load**: 80% reduction in decision points during file saving
- **Automation Success**: 80% of routine file naming handled automatically

---

*Version History:*
- v01 - 2025-03-03: Initial standards document created
