# FOMO Project Checklist

This checklist will serve as a living document that you can update as the FOMO project progresses. It provides a clear overview of completed tasks, upcoming work, and important decisions made along the way.

## Project Setup

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

## Research & Analysis

- [x] Review existing naming convention research
- [x] Identify preferred naming convention (kebab-case)
- [x] Decide on date and version formats
- [x] Analyse current file organisation system
- [x] Identify high-value automation opportunities
- [x] Map file creation sources and destinations
- [x] Complete workflow analysis section in Implementation Plan

---

## Deliverables

### Artefact Creation

- [x] Project Setup Plan
- [x] Project Charter
- [x] Naming Standards
- [x] Directory Structure
- [x] Process Flow Diagram
- [x] Implementation Plan
- [ ] Automation Overview (of All Scripts) — start after all scripts are developed
- [ ] Special Cases
- [ ] Naming Cheatsheet
- [x] Maintenance Log

### Workflow and Process Analysis

- [x] Map file creation sources and destinations
- [ ] Document 3-5 key workflow patterns
- [ ] Identify manual tasks for potential automation
- [ ] Analyse bottlenecks in current system
- [ ] Create workflow diagrams for documentation
- [ ] Validate workflow assumptions with test cases

### Automation Tools & Scripts

- [ ] Develop file system analysis scripts
- [ ] Create directory structure visualisation tools
- [x] Build naming convention validation scripts
- [ ] Develop compliance reporting tools
- [ ] Test automation scripts in isolated environment
- [ ] Document scripting patterns and examples

1. **File Analysis Tools** (Core Utilities)
   - [x] `file_utilites.sh` - Type detection, metadata extraction
   - [x] `content_utilites.sh` - Content extraction, title/keyword parsing
   - [x] `string_utilites.sh` - Case formatting, smart truncation
   - [x] `directory_utilites.sh` - Pattern analysis, duplicate detection

2. **Integration Layer**
   - [ ] `rename_utilites.sh` - Main logic for coordinating renaming operations
   - [ ] `ai_integration.sh` - Prompt template management and AI response handling

3. **Command-line Interface**
   - [ ] `ai-rename.sh` - User-friendly entry point with argument handling
   - [ ] `config.sh` - Configuration management


4. **File Type Detection** (`file_utilites.sh`):
   - Comprehensive file type detection based on extensions
   - Metadata extraction (size, creation/modification dates)
   - Binary/text file detection
   - Cross-platform compatibility for macOS and iOS
   
5. **Content Extraction** (`content_utilites.sh`):
   - Text extraction from various file formats
   - PDF support via `pdftotext`
   - Title and keyword extraction from content
   - Content similarity comparison
   
6. **String Manipulation** (`string_utilites.sh`):
   - Multiple case formats (kebab, snake, camel, pascal, etc.)
   - Smart truncation thatå preserves word boundaries
   - Filename cleaning and sanitization
   - Common prefix detection
   - Version extraction
   
7. **Directory Analysis** (`directory_utilites.sh`):
   - Pattern analysis across files
   - Duplicate detection based on size and content
   - Recommendations generation
   - Markdown report creation


---

## Implementation Status

### Phase 1: Foundation Setup

- [ ] Finalise all core documents
- [x] Set up directory structure for test area
- [x] Create basic automation scripts
- [x] Establish maintenance log structure
- [x] Begin initial testing with sample files
- [x] Establish maintenance log structure

### Phase 2: Files Implementation

- [ ] Apply conventions to all new files
- [x] Set up Hazel rules for Downloads folder
- [ ] Create Shortcuts for screenshots and common file types
- [x] Test automation on small batches of files - Initial testing with ~20 files completed
- [ ] Test automation on small batches of files

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

---

## Now! & Next?

### Parking Lot (Ideas for Later?)

- Integration with cloud storage services
- Advanced metadata tagging system
- Client portal organisation schema
- AI-assisted file categorisation
- Expanded font management system

### Open Questions (Needs Attention Now!)

- What's the best approach for handling client project archives?
- How to manage large design asset libraries efficiently?
- Which automation tool is best suited for batch operations?
- How to handle legacy files that don't conform to new standards?
- How to balance domain-specific naming conventions with system-wide standards?
- How to incorporate design-specific state indicators into naming patterns?

> **Project Management** remember to:
> - Weekly checklist review and update
> - Session summary after each significant conversation
> - Maintain log of decisions and changes
> - Track blockers and open questions
> - Schedule regular check-ins on project progress
> - Update project timeline as needed

> **Versioning & Documentation** remember to:
> - Establish version numbering system for all artefacts
> - Create version history sections in all documents
> - Document significant changes between versions
> - Implement artefact updating procedure for minor changes - Via maintenance log
> - Set criteria for creating new document versions
> - Develop cross-referencing between related documents
> - Create changelog for tracking all document updates


### Next Steps

1. Enhance Naming Standards document with design-specific patterns
2. Conduct focused workflow analysis for 3-5 key processes
3. Create simple directory structure for test implementation
4. Expand automation capabilities for design files
5. Set up test directory with sample files
6. Fix emoji handling issues in screenshot Hazel rule
6. Set up test directory with sample files

---

This checklist will be updated throughout the project.
*Last update: 2025-03-28*
- 2025-03-03: Decided to use kebab-case as the primary naming convention based on research
- 2025-03-03: Identified screenshots and downloads as high-priority automation targets
- 2025-03-03: Established v01, v02 format with leading zeros for versioning
- 2025-03-03: Selected ISO 8601 (YYYYMMDD) for date formatting in filenames
- 2025-03-05: Identified need to enhance naming standards for design files
- 2025-03-28: Verified all system symlinks are correctly established and functioning
