# FOMO Project Starter & Status

The File Organisation, Management & Optimisation (FOMO) system is a structured framework designed to establish:
- Clear naming conventions and directory structures
- Balanced human readability with machine processing requirements
- Consistent application and automation across personal and professional contexts

## Getting Started

The Getting Started section provides an entry point for understanding the FOMO system framework. For detailed implementation guidance, refer to the specific documentation referenced below.

1. Review the `Project Charter` for scope and guiding principles
3. Reference the `Project Status/Checklist` for current progress and next steps
4. Consult `Project Structure` for understanding the project organisation
4. Examine `Standards & Guidelines` documents for specific implementation guidelines

### Key Documents
1. Project Documents:
    - Project Charter (`fomo-project-charter.md`) - Strategic overview and vision
    - Project Setup Plan (`fomo-project-setup-plan.md`) - detailed setup plans and implementation guide
    - Project Structure (`fomo-project-structure-20250328.md`) - Project Directory map and organisation

2. Standards & Guidelines:
    - Naming Standards (`fomo-naming-STANDARDS-v##.md`) - Filename formatting rules
    - Directory Structure Guidelines (`fomo-directory-structure-GUIDELINES-v##.md`) - Folder hierarchy
    - Controlled Vocabulary (`fomo-controlled-VOCABULARY-v##.md`) - Taxonomy and Terminology standardisation

3. Progress Tracking:
    - Maintenance Log (`fomo-project-maintenance-log.md`) - Implementation history and change log
    - This Document: Project Starter & Status (`fomo-project-starter-and-status.md`) - Quick starter guide, checklist, task tracking and progress

### Offsite Locations

The FOMO system maintains two essential off-site locations. These act as centralised resources, providing system-wide and cross-project functionality. When onboarding, please review these two key locations.

1. **Documentation Repository** (`~/Knowledge/docs/`)
    - Contains standardised guidelines and reference documents
    - Houses language and domain-specific standards
    - Serves as a centralised knowledge base for the project
    - Requires regular updates to maintain accuracy

2. **Scripts Library** (`~/System/scripts/`)  
    - Centralised location for all automation scripts
    - Organised by language/platform (AppleScript, Python, Shell, etc.)
    - Includes complete bundles and standalone utilities
    - Critical for maintaining system automation

---

## Project Status/Checklist

This checklist aim to reflect the project status, will serve as a living document to reflect the FOMO project progresses. It provides a clear overview of completed tasks, upcoming work, and important decisions made along the way.

### Initialisation 

```
###  Project Setup

- [x] Define project scope and objectives
- [x] Create project setup plan
- [x] Create project charter
- [x] Establish conversation structure
- [x] Define essential artefacts
- [x] Identify key technical decisions
- [x] Set up project folder structure
- [x] Create test area for implementation

### Github Setup

- [x] Establish GitHub repository for FOMO system
- [x] Create basic repository structure
- [x] Connect repository to Claude project
- [x] Set up documentation synchronisation workflow
- [x] Establish version control workflow between Claude and GitHub

###  Research & Analysis

- [x] Review existing naming convention research
- [x] Identify preferred naming convention (kebab-case)
- [x] Decide on date and version formats
- [x] Analyse current file organisation system
- [x] Identify high-value automation opportunities
- [x] Map file creation sources and destinations
- [x] Complete workflow analysis section in Implementation Plan
```

### Deliverables

```
### Artefact Creation

- [x] Project Setup Plan
- [x] Project Charter
- [x] Naming Standards
- [x] Directory Structure
- [x] Process Flow Diagram
- [x] Implementation Plan
- [x] Controlled Vocabulary
- [ ] Automation Overview (summary of all Scripts) — start after scripts are developed
- [ ] Special Cases
- [ ] Naming Cheatsheet
- [x] Maintenance Log

### Workflow and Process Analysis

- [x] Map file creation sources and destinations
- [x] Identify manual tasks for potential automation
- [x] Document 3-5 key workflow patterns
- [x] Analyse bottlenecks in current system
- [x] Create workflow diagrams for documentation
- [x] Validate workflow assumptions with test cases

### Automation Tools & Scripts

- [x] Develop file system analysis scripts
- [x] Create directory structure visualisation tools
- [x] Build naming convention validation scripts
- [x] Develop compliance reporting tools
- [x] Test automation scripts in isolated environment
- [x] Document scripting patterns and examples
```

### Implementation Status

```
### Phase 1: Foundation Setup

- [x] Finalise all core documents
- [x] Set up directory structure for test area
- [x] Create basic automation scripts
- [x] Establish maintenance log structure
- [x] Begin initial testing with sample files

### Phase 2: Files Implementation

- [x] Apply conventions to all new files
- [x] Set up Hazel rules for Downloads folder
- [ ] Create Shortcuts for screenshots and common file types
- [x] Test automation on small batches of files - Initial testing with ~20 files completed
- [ ] Implement tag management guidelines
- [ ] Complete special cases documentation

### Phase 3: Active Projects

- [ ] Implement standards on current active projects
- [ ] Update references in documents
- [ ] Apply directory structure to working folders
- [ ] Refine automation based on real-world usage

### Phase 4: Historical Content

- [ ] Define approach for historical content migration
- [ ] Prioritise high-value historical content
- [ ] Document exceptions for legacy systems
- [ ] Schedule regular review sessions
```


## Project Management Process

```
**Project Management** remember to: 

- Weekly checklist review and update
- Session summary after each significant conversation
- Maintain log of decisions and changes
- Track blockers and open questions
- Schedule regular check-ins on project progress
- Update project timeline as needed

**Versioning & Documentation** remember to:

- Establish version numbering system for all artefacts
- Create version history sections in all documents
- Document significant changes between versions
- Implement artefact updating procedure for minor changes - Via maintenance log
- Set criteria for creating new document versions
- Develop cross-referencing between related documents
- Create changelog for tracking all document updates

### Offsite Location Management

**Documentation Repository** (`~/Knowledge/docs/`)

- Maintain standardised guidelines
- Keep reference documents updated
- Apply naming standards consistently to all document 
- Smart truncation that preserves word boundaries
completeness

**Scripts Library** (`~/System/scripts/`)

- Centralise all automation scripts
- Maintain script directory structure by language/type
- Document all scripts with consistent headers and usage notes
- Perform monthly testing of critical automation scripts

**Implemented Automation Tools**

- **File Naming and Processing**
  - `~/System/scripts/Bundle/sh-warp-ai-rename/` - Complete file renaming automation suite
  - `~/System/scripts/ShellScript/ai-batch-renamer.sh` - Batch file renaming with naming standards
  - `~/System/scripts/ShellScript/file-renamer.sh` - Rule-based file renaming utility
  - `~/System/scripts/Python/file-renamer.py` - Cross-platform file renaming tool

- **Analysis and Visualisation**
  - `~/System/scripts/Python/directory-checker.py` - Directory compliance verification
  - `~/System/scripts/Python/directory-visualiser.py` - Visual directory structure generation
  - `~/System/scripts/Mermaid/` - Workflow and process diagrams

- **Workflow Automation**
  - `~/System/scripts/Warp-Workflows/` - Standardised terminal workflows
  - `~/System/scripts/ShellScript/ocr-processor.sh` - Text extraction from images
  - `~/System/scripts/Bundle/sh-app-usage-auditor/` - Application usage pattern analysis

**Cross-Location Management**

- Establish synchronisation procedures between main project and offsite locations
- Implement verification process for offsite script testing
- Create documentation for managing offsite dependencies
- Schedule regular reviews of offsite content alignment
```

## Now & Next

### Open Questions 
> Food for thought

- What's the best approach for handling client project archives?
- How to manage large design asset libraries efficiently?
- Which automation tool is best suited for batch operations?
- How to handle legacy files that don't conform to new standards?
- How to balance domain-specific naming conventions with system-wide standards?
- How to incorporate design-specific state indicators into naming patterns?
- How to establish consistent implementation of controlled vocabulary across domains?
- What's the best approach for screenshot handling and automation?
- How to maintain synchronisation between main project and offsite locations?
- What verification process should be established for offsite script testing?

### Parking Lot 
> Ideas for Later

- Integration with cloud storage services
- Advanced metadata tagging system
- Client portal organisation schema
- AI-assisted file categorisation
- Expanded font management system

### Next Steps
> Actions Needs Attention Now

1. Develop special cases documentation for edge cases and exceptions
2. Establish comprehensive design asset organisation guidelines
3. Create domain-specific implementation standards
4. Fix emoji handling issues in screenshot Hazel rule
5. Refine integration between controlled vocabulary and automation tools
6. Create testing framework for cross-location script verification

---

## Change Log
- 2025-03-03: Decided to use kebab-case as the primary naming convention based on research
- 2025-03-03: Identified screenshots and downloads as high-priority automation targets
- 2025-03-03: Established v01, v02 format with leading zeros for versioning
- 2025-03-03: Selected ISO 8601 (YYYYMMDD) for date formatting in filenames
- 2025-03-05: Identified need to enhance naming standards for design files
- 2025-03-28: Verified all system symlinks are correctly established and functioning
- 2025-03-30: Completed Version 1 of controlled vocabulary documentation
- 2025-03-30: Identified three priority areas: automation implementation, special cases documentation, and controlled vocabulary integration
- 2025-03-30: Revised implementation checklist based on comprehensive documentation review
- 2025-03-31: Added tracking for offsite locations at ~/Knowledge/docs/ and ~/System/scripts/
- 2025-03-31: Added Quick Start guide to checklist document for improved accessibility
- 2025-04-01: Completed all workflow analysis tasks and process documentation
- 2025-04-01: Finalised all core automation tools and scripts for file management
- 2025-04-01: Updated project status to reflect completed workflow and automation tasks
- 2025-04-01: Refined Next Steps to focus on special cases, design assets, and integration refinements
---

*Version History:*
- v01 - 2025-03-03: Initial document created (as fomo-project-checklist.md)
- v02 - 2025-03-30: Updated with project status and priority areas
- v03 - 2025-03-31: Added Quick Start guide and offsite locations tracking
- v04 - 2025-04-01: Renamed to fomo-project-starter-and-status.md and updated with completed workflow and automation tasks
