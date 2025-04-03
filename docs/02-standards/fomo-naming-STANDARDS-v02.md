# FOMO Naming Standards v02

## 1. Introduction and Purpose

### 1.1 Purpose

This document establishes the file naming conventions for the File Organisation, Management & Optimisation (FOMO) project. It provides a comprehensive framework to ensure files are named consistently, meaningfully, and in a way that balances human readability with machine processing requirements while accommodating domain-specific needs.

### 1.2 Scope

These naming standards apply to:

- Design projects and assets (including fonts, mock-ups, and client deliverables)
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
- Improve client communication with professional file delivery
- Streamline design-development handoffs

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

### 2.7 Domain Awareness

Recognise and respect established industry standards and tool requirements in specialised domains like design and development.

## 3. Layered Naming Approach

The FOMO naming system follows a layered approach, with general rules that apply across the system and domain-specific adaptations that respect established practices in specialised fields.

### 3.1 General Rules (Level 1)

These core rules apply to most files within the system:

- Use lowercase kebab-case as the default format
- Follow ISO 8601 date format (yyyyMMdd) for chronological information
- Use v## version numbering with leading zeros
- Avoid special characters except when specified

### 3.2 Domain-Specific Adaptations (Level 2)

Specialised domains may follow variations of the general rules where established industry practices or tool requirements dictate:

- **Design Files**: Allow for tool-specific naming patterns and client identification
- **Font Files**: Use PascalCase for font families following typography standards
- **Development Files**: Follow language-specific conventions (such as PascalCase for React components)
- **Client Deliverables**: Include clear client identification and approval status

## 4. Technical Specifications

### 4.1 Case Format

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

**Domain-Specific Exceptions:**

- Font files use PascalCase for font family names
- React components use PascalCase
- Python files use snake_case
- Design tools with fixed naming patterns should be followed for compatibility

### 4.2 Client Identification

For client-facing projects, include a client identifier:

- Use a 2-4 letter abbreviation for the client name
- Place at the beginning of the filename
- Separate from the rest of the name with a hyphen

Examples:

```
acme-homepage-banner-v01.jpg
ibm-presentation-quarterly-20250301-v02.pptx
xyz-contract-agreement-20250215.pdf
```

### 4.3 Date Format

Use ISO 8601 format (yyyyMMdd) without separators:

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

### 4.4 Version Numbering

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

**Design Workflow Specifics:**
For design files requiring extensive revisions or approval cycles, use a more detailed versioning approach:

- Draft versions: `v01-draft`, `v02-draft`
- Review versions: `v01-review`, `v02-review`
- Client feedback: `v01-client`, `v02-client`
- Approved versions: `v01-approved`
- Production versions: `v01-production`

Examples:

```
acme-logo-primary-v03-client.ai
acme-logo-primary-v04-approved.ai
acme-website-homepage-v02-review.sketch
```

### 4.5 Special Characters

- **Allowed characters**:
  - Hyphens `-` for word separation
  - Periods `.` for file extensions and specific uses (e.g., language codes)
  - Underscores `_` only for specific cases like pixel density indicators
  - Square brackets `[]` only for font axis notations in variable fonts
- **Prohibited characters**:`!@#$%^&*()=+[]{};:'"\|,/<>?` and `spaces`

## 6. Order of the Components

The order of components in filenames follows a logical progression that balances identification, context, and technical metadata:

1.  **Project or Context Identifier** (First Position)
    - Immediately establishes the broader context
    - Enables quick filtering when working across multiple projects
    - Examples: project code, client name, application name
2.  **Content Type** (Second Position)
    - Identifies what the file actually is
    - Creates natural grouping of similar file types
    - Examples: report, logo, screenshot, meeting
3.  **Descriptive Elements** (Middle Positions)
    - Provides specific identifying information
    - Differentiates between similar files
    - Examples: homepage, dark-version, quarterly
4.  **Technical Metadata** (Later Positions)
    - Date information (yyyyMMdd)
    - Sequential identifiers or specific technical details
    - Pixel dimensions or other technical specifications
5.  **Version Information** (Final Position, Before Extension)
    - Version number (v01, v02)
    - Status indicators where appropriate
    - Always the last element before the file extension

This ordering ensures the most human-relevant information appears first, creating scannable file lists, while technical details that aid in sorting and versioning appear later in the name.

## 6. Naming Patterns by File Type

### 6.1 Documents and Reports

Pattern: `[client]-[project]-[type]-[descriptor]-[yyyyMMdd]-v[##].[ext]`

Examples:

```
fomo-report-quarterly-20250301-v02.pdf
acme-website-brief-redesign-20250215-v01.docx
ibm-app-proposal-mobile-202503-v03.md
```

### 6.2 Meeting Notes and Communications

Pattern: `[client]-[meeting-type]-[context]-[yyyyMMdd].[ext]`

Examples:

```
acme-meeting-kickoff-20250310.md
ibm-call-feedback-20250322.md
xyz-workshop-planning-20250405.md
```

### 6.3 Screenshots and Captures

Pattern: `screenshot-[context]-[yyyyMMdd]-[##/HHMMSS].[ext]`

Examples:

```
screenshot-safari-github-awesome-20250301-02.png
screenshot-error-message-20251203-143022.png
screenshot-iphone-app-checkout-20250302-v01.png
```

### 6.4 Design Assets

Pattern: `[client]-[asset-type]-[descriptor]-[state]-v[##].[ext]`

Examples:

```
acme-logo-primary-v03.svg
ibm-banner-homepage-v01.jpg
xyz-icon-download-v02.png
acme-mockup-homepage-v02-review.jpg
```

### 6.5 Design Source Files

Pattern: `[client]-[project]-[component]-[state]-v[##].[ext]`

Examples:

```
acme-website-homepage-v03.sketch
ibm-app-profile-page-v02-draft.psd
xyz-campaign-email-header-v01-approved.ai
```

### 6.6 Font Files

For font files, follow typography industry standards:

**Static Fonts:**
Pattern: `FontFamilyName-StyleName.[ext]`

Examples:

```
SourceSansPro-Regular.ttf
SourceSansPro-Bold.ttf
SourceSansPro-Italic.ttf
```

**Variable Fonts:**
Pattern: `FontFamilyName[axis1,axis2].[ext]` or `FontFamilyName-Italic[axis1,axis2].[ext]`

Examples:

```
SourceSansPro[wght].ttf
SourceSansPro-Italic[wght].ttf
RobotoFlex[GRAD,wght].ttf
```

**Font Versioning:**
Store version information in the directory structure rather than the filename:

```
/FontLibrary/
├── SourceSansPro/
│   ├── Static/
│   │   ├── v3.1.2/
│   │   │   ├── SourceSansPro-Regular.otf
│   │   ├── v3.2.0/
│   │   │   ├── SourceSansPro-Regular.otf
```

### 6.7 Code and Development Files

Pattern: `[function/purpose]-[language].[ext]` or follow language conventions

Examples:

```
file-renamer.py
api-client.js
UserProfile.tsx  # React component using PascalCase
database_connector.py  # Python file using snake_case
```

### 6.8 Configuration Files

Follow standard naming conventions for the platform or maintain established names

Examples:

```
.env-production
.env-development
docker-compose.yml
tsconfig.json
```

## 7. Design-Specific Workflows

### 7.1 Client Feedback Cycles

For design files going through iterative client feedback:

Pattern: `[client]-[project]-[component]-v[##]-[feedback-round].[ext]`

Examples:

```
acme-website-homepage-v01-round1.sketch
acme-website-homepage-v01-round2.sketch
acme-logo-primary-v02-feedback.ai
```

### 7.2 Design States

Design files should include state indicators that reflect their position in the workflow:

- **Draft**: Initial or work-in-progress versions (`draft`)
- **Internal Review**: Ready for team review (`review`)
- **Client Review**: Sent to client for feedback (`client`)
- **Revision**: Updated based on feedback (`revision`)
- **Approved**: Signed off by client (`approved`)
- **Production**: Ready for implementation (`production`)
- **Archive**: Final version for record-keeping (`archive`)

Example workflow sequence:

```
acme-website-homepage-v01-draft.sketch
acme-website-homepage-v01-review.sketch
acme-website-homepage-v01-client.sketch
acme-website-homepage-v02-revision.sketch
acme-website-homepage-v02-approved.sketch
acme-website-homepage-v02-production.sketch
```

### 7.3 Design-Development Handoff

Files intended for developer implementation should use a specific naming pattern:

Pattern: `[client]-[project]-[component]-handoff-v[##].[ext]`

Examples:

```
acme-website-homepage-handoff-v02.sketch
ibm-app-navigation-handoff-v03.xd
xyz-campaign-email-handoff-v01.fig
```

### 7.4 Collaborative Design Work

When multiple designers work on the same file, include designer initials:

Pattern: `[client]-[project]-[component]-[designer-initials]-v[##].[ext]`

Examples:

```
acme-website-homepage-jd-v01.sketch
acme-website-homepage-mk-v01.sketch
ibm-app-profile-ab-v02.xd
```

## 8. Special Cases and Exceptions

### 8.1 Multilingual Files

For files available in multiple languages, add the ISO 639-1 language code before the extension:

Examples:

```
user-guide.en.pdf
user-guide.fr.pdf
product-description.en-au.md
```

### 8.2 Temporary Files & Backups

Prefix with `tmp-` and `bak-` include date to facilitate cleanup or storage:

Examples:

```
tmp-export-data-20250315.csv
tmp-image-processing-20250310.png
bak-webstie-arworks-20221220.zip
```

### 8.3 Framework-Specific Files

When working within frameworks with established conventions, follow the framework's standards:

Examples:

```
# React components (PascalCase)
ButtonGroup.tsx
UserProfile.js

# Python modules (snake_case)
database_connector.py
```

### 8.4 Pixel Density Indicators

For images with different pixel densities, use an underscore followed by the density:

Examples:

```
icon-menu_2x.png
logo-small_3x.png
```

### 8.5 Adobe Creative Cloud Files

For Adobe CC files, follow Adobe's auto-save and versioning patterns when necessary:

Examples:

```
project-name.ai
project-name-1.ai  # Auto-saved version
project-name.ai.idlk  # Lock file
```

## 9. Implementation Guidelines

### 9.1 New Files

- Apply these naming conventions to all new files immediately
- Configure save dialogs and templates to default to these patterns
- Use automation tools to enforce naming on file creation

### 9.2 Existing Files

- Prioritise renaming active project files
- Use batch renaming tools for bulk updates
- Address high-value historical content as resources permit

### 9.3 Automation Tools

- Configure Hazel rules to automatically rename files based on these standards
- Create Shortcuts for streamlined naming during save operations
- Develop Python scripts for batch processing and compliance checking
- Set up n8n workflows for integrated file processing
- Create design tool templates with naming presets

### 9.4 Design Tool Integration

- Create Adobe Creative Cloud templates with proper naming structures
- Configure Sketch, Figma, and XD default naming patterns
- Develop scripts for batch renaming design assets
- Set up font management tools to follow the specified conventions

### 9.5 Version Control Integration

- Ensure naming conventions align with version control best practices
- Configure git hooks to validate file names before commit
- Document any special considerations for repository organisation
- Create specific .gitignore patterns for design tool temporary files

## 10. Examples and Templates

### 10.1 Design Project Example

```
acme-website/
├── briefs/
│   ├── acme-website-brief-initial-20250301-v01.pdf
│   └── acme-website-brief-revised-20250315-v02.pdf
├── design/
│   ├── acme-website-wireframes-homepage-v01-draft.sketch
│   ├── acme-website-wireframes-homepage-v02-client.sketch
│   ├── acme-website-mockup-homepage-v01-draft.psd
│   └── acme-website-style-guide-v01-approved.pdf
├── assets/
│   ├── acme-logo-primary-v01.svg
│   ├── acme-logo-secondary-v01.svg
│   ├── acme-hero-homepage-v01.jpg
│   └── acme-icon-set-v01.ai
└── production/
    ├── acme-website-homepage-handoff-v02.sketch
    ├── acme-website-assets-handoff-v01.zip
    └── acme-website-specs-20250401.pdf
```

### 10.2 Font Management Example

```
FontLibrary/
├── SourceSansPro/
│   ├── Static/
│   │   ├── v3.1.2/
│   │   │   ├── SourceSansPro-Regular.otf
│   │   │   ├── SourceSansPro-Bold.otf
│   │   │   └── SourceSansPro-Italic.otf
│   ├── Variable/
│   │   ├── v3.1.2/
│   │   │   ├── SourceSansPro[wght].otf
│   │   │   └── SourceSansPro-Italic[wght].otf
└── RobotoFlex/
    └── Variable/
        ├── v2.0.1/
        │   └── RobotoFlex[GRAD,wght].otf
```

### 10.3 Development Project Example

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

### 10.4 Client Feedback Cycle Example

```
project-timeline:
1. acme-logo-primary-v01-draft.ai (Initial concept)
2. acme-logo-primary-v01-review.ai (Internal team review)
3. acme-logo-primary-v01-client.ai (Sent to client)
4. acme-logo-primary-v02-revision.ai (Updated per feedback)
5. acme-logo-primary-v02-client.ai (Second client review)
6. acme-logo-primary-v03-revision.ai (Final adjustments)
7. acme-logo-primary-v03-approved.ai (Client approval)
8. acme-logo-primary-v03-production.ai (Production-ready)
```

### 10.5 Personal Files Example

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

## 11. Maintenance and Governance

### 11.1 Regular Audits

- Conduct monthly checks of recently created files
- Use automated tools to measure compliance
- Review naming patterns for effectiveness and usability

### 11.2 Updates and Revisions

- Document challenges and solutions in the Maintenance Log
- Refine standards based on practical experience
- Version this document for significant changes

### 11.3 Exceptions Management

- Document necessary exceptions in the Special Cases document
- Maintain a registry of approved variations
- Review exceptions periodically for patterns that might indicate needed changes

## 12. Integration with Other FOMO Documents

This Naming Standards document works in conjunction with other FOMO project documents to form a unified system:

- **fomo-project-charter-v##.md**: Establishes the overall vision and principles for the fomo system
- **fomo-naming-standards-v##.md**: (this document) Defines the file naming conventions used within this structure
- **fomo-directory-structure-v##.md**: Defines the folder hierarchy these named files will live within
- **Implementation-Plan-v01.md**: Outlines the phased approach to implementing these standards
- **Automation-Scripts-v01.md**: Contains scripts and tools to enforce these naming conventions
- **Special-Cases-v01.md**: Provides detailed guidance for exceptions to these standards
- **Naming-Cheatsheet-v01.md**: Quick reference guide for daily application

## 13. Success Measures

The effectiveness of these naming standards will be measured by:

- **File Location Time**: 50% reduction in time to locate specific files
- **Naming Compliance**: 95% of new files following conventions
- **Cognitive Load**: 80% reduction in decision points during file saving
- **Automation Success**: 80% of routine file naming handled automatically
- **Workflow Efficiency**: 40% reduction in time spent managing design or development file
- **Cross-functional Clarity**: 70% improvement in design-development handoff efficiency

---

_Version History:_

- v01 - 2025-03-03: Initial standards document created
- v02 - 2025-03-08: Enhanced with design-specific workflows, font management standards, and client feedback cycle support. Added layered naming approach and domain-specific adaptations.
