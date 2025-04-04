# Hazel Rules Overview Draft (for reference only)

## Table of Contents
1. [Introduction](#introduction)
2. [Rule Categories](#rule-categories)
3. [Rule Definitions](#rule-definitions)
4. [Implementation Priorities](#implementation-priorities)
5. [Testing Plans](#testing-plans)
6. [Appendix](#appendix)

## Introduction

This document outlines the specification for Hazel Rules within the FOMO (File Organisation, Management & Optimisation) system. Hazel is a folder-watching utility for macOS that automates file management tasks based on predefined rules and conditions. These rules form a critical component of the FOMO automation workflow.

### Purpose

The primary purposes of implementing Hazel Rules in the FOMO system are:
- Automate file renaming in designated folders to ensure naming convention compliance
- Sort files based on type (e.g., PDFs, images, documents) into appropriate directories
- Trigger additional workflows such as image optimisation and metadata updates
- Reduce manual processing and maintain consistency across the file system

### Scope

This specification covers all planned Hazel rule configurations, their conditions, actions, and implementation priorities. It serves as the authoritative reference for developing and maintaining the Hazel rules component of the FOMO system.

## Rule Categories

Hazel Rules in the FOMO system are organised into the following categories:

1. **File Naming Rules**: Ensure files follow the established naming conventions
2. **File Sorting Rules**: Categorise and move files based on their types and attributes
3. **Cleanup Rules**: Remove temporary files and manage duplicates
4. **Workflow Trigger Rules**: Initiate external scripts and processes for further automation
5. **Metadata Management Rules**: Update and standardise file metadata

## Rule Definitions

### File Naming Rules

| Rule ID | Name | Monitored Folder | Conditions | Actions | Description |
|---------|------|------------------|------------|---------|-------------|
| FN-001 | Date Prefix for Documents | ~/Downloads | Kind is PDF, Word Document, or Text | Rename with pattern "YYYY-MM-DD_[filename].[ext]" | Adds date prefix to document files |
| FN-002 | Image File Standardisation | ~/Pictures | Kind is Image | Rename with pattern "YYYY-MM-DD_IMG_[n].[ext]" where [n] is sequential number | Standardises image filenames |
| FN-003 | Invoice Naming Convention | ~/Downloads | Name contains "invoice", "receipt", or matches regex "INV-\d+" | Rename with pattern "YYYY-MM-DD_Invoice_[Vendor].[ext]" | Standardises invoice filenames |
| FN-004 | Report Standardisation | ~/Documents | Name contains "report", "analysis", or "summary" | Rename with pattern "YYYY-MM-DD_Report_[Topic].[ext]" | Standardises report filenames |

### File Sorting Rules

| Rule ID | Name | Monitored Folder | Conditions | Actions | Description |
|---------|------|------------------|------------|---------|-------------|
| FS-001 | PDF Organiser | ~/Downloads | Kind is PDF | Move to ~/Documents/PDFs | Moves PDF files to dedicated folder |
| FS-002 | Image Sorter | ~/Downloads | Kind is Image | Move to ~/Pictures/Imports | Moves image files to dedicated folder |
| FS-003 | Document Type Sorter | ~/Documents | Kind is specific document type | Move to ~/Documents/[Type] | Sorts documents by file type |
| FS-004 | Financial Document Organiser | ~/Downloads | Name contains "invoice", "statement", "receipt" | Move to ~/Documents/Financial/[Current Year] | Organises financial documents by year |
| FS-005 | Archive Old Files | ~/Documents | Date modified is older than 1 year | Move to ~/Documents/Archive/[Year] | Archives older documents by year |

### Cleanup Rules

| Rule ID | Name | Monitored Folder | Conditions | Actions | Description |
|---------|------|------------------|------------|---------|-------------|
| CL-001 | Remove Temporary Files | ~/Downloads | Extension is tmp, temp, or .DS_Store | Delete | Removes temporary system files |
| CL-002 | Clear Old Downloads | ~/Downloads | Date added is older than 30 days | Move to ~/Downloads/Old | Clears download folder of aged files |
| CL-003 | Screenshot Cleanup | ~/Desktop | Filename contains "Screen Shot" | Move to ~/Pictures/Screenshots after 1 day | Manages desktop screenshots |
| CL-004 | Duplicate File Handler | Various folders | Is duplicate (based on content) | Move to ~/Duplicates | Identifies and segregates duplicate files |

### Workflow Trigger Rules

| Rule ID | Name | Monitored Folder | Conditions | Actions | Description |
|---------|------|------------------|------------|---------|-------------|
| WT-001 | Image Optimisation Trigger | ~/Pictures/Imports | Kind is Image AND size is greater than 1MB | Run AppleScript "Image_Optimiser.scpt" | Triggers image optimisation script |
| WT-002 | PDF OCR Processing | ~/Documents/PDFs | Kind is PDF AND text is not searchable | Run Shell Script "pdf_ocr.sh" | Triggers OCR processing for PDFs |
| WT-003 | Video Compression | ~/Movies/Imports | Kind is Video AND size is greater than 100MB | Run Shell Script "video_compressor.sh" | Triggers video compression workflow |
| WT-004 | Compliance Validator | Various folders | Any file | Run Python Script "naming_validator.py" | Validates file naming compliance |

### Metadata Management Rules

| Rule ID | Name | Monitored Folder | Conditions | Actions | Description |
|---------|------|------------------|------------|---------|-------------|
| MM-001 | Add Creator Tag | Various folders | Any file | Add tag "Creator: [username]" | Adds creator metadata |
| MM-002 | Project Assignment | Various folders | Name contains project code | Add tags based on project codes | Categorises files by project |
| MM-003 | Content Type Tagging | Various folders | Based on file type | Add content type tag | Categorises by content type |
| MM-004 | Status Tagging | ~/Documents/WIP | Any file | Add "In Progress" tag | Marks work in progress files |

## Implementation Priorities

The implementation of Hazel Rules will be phased according to the following priority levels:

### Phase 1: Essential Organisation (High Priority)
- File Naming Rules (FN-001, FN-002)
- Basic File Sorting Rules (FS-001, FS-002)
- Critical Cleanup Rules (CL-001, CL-003)

### Phase 2: Enhanced Organisation (Medium Priority)
- Advanced File Naming Rules (FN-003, FN-004)
- Additional File Sorting Rules (FS-003, FS-004)
- Additional Cleanup Rules (CL-002, CL-004)
- Basic Metadata Management (MM-001, MM-004)

### Phase 3: Workflow Integration (Lower Priority)
- All Workflow Trigger Rules (WT-001 through WT-004)
- Advanced Metadata Management (MM-002, MM-003)
- Archive Rules (FS-005)

## Testing Plans

### Unit Testing

Each Hazel rule will be tested individually using the following methodology:

1. **Setup**: Create test files that match the rule conditions
2. **Execution**: Place test files in the monitored folder
3. **Verification**: Confirm the rule executes the expected actions
4. **Documentation**: Record results and any adjustments needed

### Integration Testing

Rules that interact with each other or external scripts will undergo integration testing:

1. **Workflow Testing**: Test sequences of rules that should trigger in succession
2. **Script Integration**: Verify proper handoff to external scripts and applications
3. **Performance Assessment**: Measure processing time and system impact
4. **Conflict Resolution**: Identify and resolve any rule conflicts

### User Acceptance Testing

Before full deployment, a pilot testing phase will involve:

1. **Controlled Environment**: Test on limited folders with real-world data
2. **User Feedback Collection**: Document user experience and issues
3. **Refinement**: Adjust rules based on feedback
4. **Documentation Update**: Update specifications based on tested outcomes

### Test Schedule

| Testing Phase | Timeline | Success Criteria | Responsible Party |
|---------------|----------|------------------|-------------------|
| Rule Development Unit Tests | Within 1 day of each rule creation | 100% of test cases pass | Developer |
| Integration Testing | After completion of each phase | 95% of workflows complete without error | QA Team |
| User Acceptance Testing | 1 week before deployment | User approval rating above 80% | End Users & QA Team |
| Post-Deployment Monitoring | 2 weeks after deployment | Error rate below 5% | Support Team |

## Appendix

### Glossary

- **Hazel**: A macOS utility that watches designated folders and performs actions on files based on rules
- **Rule**: A set of conditions and corresponding actions to be performed when conditions are met
- **Condition**: A criterion that must be true for a rule to trigger (e.g., file type, name, size)
- **Action**: An operation performed when all conditions are met (e.g., rename, move, tag)
- **Workflow**: A sequence of automated processes that may involve multiple rules and external scripts

### References

- FOMO System Guidelines
- Hazel Documentation (https://www.noodlesoft.com/manual/)
- FOMO Naming Standards Document
- Apple Script Integration Guidelines

