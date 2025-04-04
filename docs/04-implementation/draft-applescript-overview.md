# AppleScript Scripts Specification

*Document Date: 20230704*

## 1. Introduction

This document outlines the specifications for AppleScript scripts to be developed as part of the FOMO (File Organisation, Management & Optimisation) system. AppleScript is chosen for its deep integration with macOS and ability to automate tasks across multiple applications. The scripts defined herein will extend Hazel's capabilities for complex file management tasks.

## 2. Script Categories

The AppleScript scripts for FOMO are categorised as follows:

1. **Image Processing Scripts** - Scripts that handle image optimisation, metadata manipulation, and format conversion
2. **Document Processing Scripts** - Scripts that process document files including PDFs, text files, and office documents
3. **Metadata Management Scripts** - Scripts specifically focused on reading, writing, and modifying file metadata
4. **System Integration Scripts** - Scripts that integrate FOMO with other macOS system components and applications
4. **Utility Scripts** - Helper scripts for diagnostic, reporting, and maintenance tasks

## 3. Script Definitions

### 3.1 Image Processing Scripts

| Script Name | Trigger | Functionality | Inputs | Outputs | Priority |
|-------------|---------|---------------|--------|---------|----------|
| ImageOptimiser | Hazel rule on image files | Compresses and optimises images while preserving quality | Image file path, target quality (0-100) | Optimised image, log entry | High |
| ImageResizer | Hazel rule or manual trigger | Resizes images to standard dimensions for various purposes | Image file path, target dimensions | Resized image, log entry | Medium |
| ImageMetadataExtractor | Hazel rule on image import | Extracts EXIF and other metadata from images for categorisation | Image file path | Metadata JSON file, updated filename with metadata | Medium |
| WebImagePrep | Hazel rule on designated folder | Prepares images for web use with appropriate compression and formatting | Image file path, target platform | Web-optimised image | Low |

### 3.2 Document Processing Scripts

| Script Name | Trigger | Functionality | Inputs | Outputs | Priority |
|-------------|---------|---------------|--------|---------|----------|
| PDFMetadataUpdater | Hazel rule on PDF files | Updates PDF metadata to comply with FOMO standards | PDF file path, metadata values | Updated PDF with standardised metadata | High |
| DocxToPDF | Hazel rule on document files | Converts Word documents to PDF format | DOCX file path | PDF file, log entry | Medium |
| TextExtractor | Hazel rule on scanned documents | Performs OCR on image-based PDFs | PDF file path | Searchable PDF, extracted text file | Medium |
| DocumentMerger | Manual trigger | Combines multiple documents into a single PDF | List of file paths, output name | Combined PDF document | Low |

### 3.3 Metadata Management Scripts

| Script Name | Trigger | Functionality | Inputs | Outputs | Priority |
|-------------|---------|---------------|--------|---------|----------|
| TagSynchroniser | Scheduled task | Ensures Finder tags match metadata tags across the file system | Directory path | Updated files with synchronised tags, log report | High |
| MetadataValidator | Hazel rule on file modification | Validates that files meet FOMO metadata standards | File path, standards profile | Validation report, fixed metadata where possible | Medium |
| BulkMetadataEditor | Manual trigger | Applies consistent metadata across multiple files | File list, metadata template | Updated files with standardised metadata | Medium |
| CategoryTagger | Hazel rule on new files | Automatically applies tags based on file content and context | File path | Tagged file, log entry | Low |

### 3.4 System Integration Scripts

| Script Name | Trigger | Functionality | Inputs | Outputs | Priority |
|-------------|---------|---------------|--------|---------|----------|
| HaselNotifier | Hazel rule completion | Sends notifications upon completion of critical Hazel tasks | Process info, status | System notification, log entry | High |
| RaycastIntegrator | Raycast or Spotlight search | Enables searching FOMO files via Raycast with enhanced metadata | Search query | Search results with rich metadata | Medium |
| iCloudSyncMonitor | Scheduled task | Monitors and reports on iCloud sync status for FOMO directories | Directory paths | Sync status report, notifications for issues | Medium |
| ShortcutBridge | Apple Shortcut triggers | Provides bridge between Apple Shortcuts and AppleScript functionality | Parameters from Shortcut | Action result, status report | Low |

### 3.5 Utility Scripts

| Script Name | Trigger | Functionality | Inputs | Outputs | Priority |
|-------------|---------|---------------|--------|---------|----------|
| FOMODiagnostics | Manual trigger or scheduled | Performs diagnostics on FOMO system components | Test scope parameters | Diagnostic report | High |
| UsageReporter | Scheduled (weekly) | Generates reports on FOMO usage statistics | Time period | Usage report with visualisations | Medium |
| DuplicateDetector | Manual trigger or scheduled | Identifies potential duplicate files across FOMO system | Directory paths | Report of potential duplicates with confidence scores | Medium |
| BackupVerifier | After backup operations | Verifies integrity of FOMO backups | Backup path, original path | Verification report, notification of issues | Low |


## 4. Integration Points with FOMO Components

### 4.1 Integration with Hazel Rules

AppleScript scripts will integrate with Hazel primarily through:
- Embedded script actions within Hazel rules
- External script files called by Hazel rules
- Notification handlers for Hazel rule completion

Key integration points:
- Image files will be processed by Hazel rules that trigger the appropriate AppleScript
- Document files will be routed to specific AppleScripts based on type and required processing
- Metadata validation will occur within Hazel's workflow

### 4.2 Integration with Apple Shortcuts

AppleScript scripts will be accessible through Apple Shortcuts via:
- Run AppleScript actions in Shortcuts
- ShortcutBridge script to handle complex parameter passing
- Shared variables and system attributes

Primary integration scenarios:
- User-initiated processing of selected files
- Batch operations triggered via Shortcuts
- Diagnostic and reporting functions accessible via Shortcuts

### 4.3 Integration with Python Scripts

AppleScript and Python scripts will complement each other through:
- AppleScript calling Python scripts for complex data processing
- Python scripts generating AppleScript code for execution
- Shared data formats and interchange standards

Key integration points:
- AppleScript handles macOS-specific functionality while Python handles heavy data processing
- Results from Python batch processing can trigger AppleScript notifications
- Both systems will use standardised logging and reporting formats

### 4.4 Integration with macOS System Components

AppleScript scripts will leverage these macOS components:
- Finder for file operations and tag management
- Spotlight for enhanced metadata and search capabilities
- Notification Center for user alerts
- Calendar for scheduled tasks
- Image and PDF rendering engines

## 5. Technical Specifications

### 5.1 Script Structure Standards

All AppleScripts will follow these structural standards:
1. Header comment block with script name, version, author, and last modified date
2. Property definitions section
3. Handler definitions section
4. Main script section
4. Error handling routines
5. Logging functionality

### 5.2 Error Handling

Scripts will implement comprehensive error handling:
- Try/on error blocks around all critical operations
- Detailed error messages with error codes
- Graceful degradation when possible
- System notifications for critical errors
- Logging of all errors to central FOMO log

### 5.3 Logging Standards

All scripts will log operations to a standardised log format:
- Timestamp
- Script name and version
- Operation performed
- Files affected
- Success/failure status
- Performance metrics where relevant

### 5.4 Security Considerations

Scripts will adhere to these security practices:
- Minimal permissions model
- Validation of all inputs
- No hardcoded credentials
- Secure handling of sensitive metadata
- Respect for user privacy settings

## 7. Future Considerations

Areas for future expansion of the AppleScript component include:
- Integration with cloud services beyond iCloud
- Enhanced machine learning capabilities for automatic categorisation
- Voice command integration via Siri
- Expanded mobile device syncing and integration
- Support for collaborative workflows

## 8. Appendices

### 8.1 Script Templates

Standard script templates will be stored in the `/Templates` directory and will include:
- Basic script structure
- Standard error handling
- Logging framework
- Common utility handlers

### 8.2 Testing Protocol

Each script will undergo testing according to the FOMO Testing Protocol which includes:
- Unit testing of individual handlers
- Integration testing with Hazel rules and other components
- Performance testing for resource-intensive operations
- Edge case validation
- User acceptance testing

