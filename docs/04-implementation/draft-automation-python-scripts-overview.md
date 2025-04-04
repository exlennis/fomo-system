# Python Scripts Overview Draft (for reference only)

*Timestamp: 20231128*

## Table of Contents
1. [Introduction](#introduction)
2. [Script Categories](#script-categories)
3. [Script Definitions](#script-definitions)
4. [Implementation Priorities](#implementation-priorities)
5. [Integration Points](#integration-points)
6. [Version Control and Maintenance](#version-control-and-maintenance)

## Introduction

This document provides detailed specifications for the Python scripts component of the FOMO (File Organization, Management & Optimization) system. The Python scripts are designed to automate bulk file operations, validate naming compliance, and generate reports on file organisation status.

## Script Categories

The Python scripts component consists of four primary categories of scripts:

| Category | Purpose | Primary Functions |
|----------|---------|------------------|
| File Renaming | Automate bulk file renaming according to FOMO naming conventions | Pattern matching, string manipulation, batch processing |
| Compliance Checking | Validate files against established naming standards | Pattern validation, recursive directory scanning, exception handling |
| Reporting | Generate compliance reports and statistics | Data aggregation, report formatting, export to various formats |
| Utility | Support other FOMO components with common functions | Configuration management, logging, error handling |

## Script Definitions

### File Renaming Scripts

#### 1. `bulk_rename.py`

**Purpose**: Rename multiple files according to FOMO naming conventions in a single operation.

**Input Parameters**:
- `--source-dir` (required): Directory containing files to be renamed
- `--pattern` (required): Naming pattern to apply (e.g., "YYYY-MM-DD_DocumentType")
- `--recursive` (optional): Flag to process subdirectories
- `--dry-run` (optional): Simulate renaming without changing files
- `--metadata-source` (optional): Extract metadata from file properties or content

**Processing Logic**:
1. Scan the source directory (and subdirectories if recursive flag is set)
2. For each file:
   - Extract relevant metadata (date, document type, etc.)
   - Generate new filename according to pattern
   - Validate new filename against FOMO standards
   - Rename file (or simulate if dry-run is enabled)
3. Generate summary of operations

**Outputs**:
- Console output of renamed files
- Log file with detailed operation results
- CSV report of all rename operations (original name, new name, status)

#### 2. `date_standardiser.py`

**Purpose**: Extract and standardise dates in filenames.

**Input Parameters**:
- `--source-dir` (required): Directory containing files to process
- `--date-format` (optional, default="YYYY-MM-DD"): Output date format
- `--extract-from` (optional): Source of date information (filename, metadata, content)
- `--recursive` (optional): Flag to process subdirectories

**Processing Logic**:
1. Identify date patterns in existing filenames or metadata
2. Parse and convert dates to standardised format
3. Apply renamed dates to filenames
4. Handle edge cases (missing dates, ambiguous formats)

**Outputs**:
- Renamed files with standardised date format
- Log of date extraction and conversion results
- Summary report of processed files

### Compliance Checking Scripts

#### 1. `compliance_validator.py`

**Purpose**: Check if files conform to FOMO naming standards and generate compliance reports.

**Input Parameters**:
- `--source-dir` (required): Directory containing files to check
- `--standards-file` (optional): JSON file containing naming standards
- `--recursive` (optional): Flag to process subdirectories
- `--strict-mode` (optional): Flag to enforce all rules without exceptions
- `--output-format` (optional): Format for compliance report (JSON, CSV, HTML)

**Processing Logic**:
1. Load naming standards from configuration
2. Recursively scan directories for files
3. For each file:
   - Parse filename components
   - Check against pattern rules
   - Validate date formats, separators, and allowed characters
   - Record compliance status and violations
4. Generate comprehensive compliance report

**Outputs**:
- Compliance report (percentage of compliant files)
- Detailed list of non-compliant files with specific rule violations
- Suggested corrections for non-compliant files

#### 2. `metadata_validator.py`

**Purpose**: Validate and ensure consistency between filename and file metadata.

**Input Parameters**:
- `--source-dir` (required): Directory containing files to validate
- `--metadata-fields` (required): List of metadata fields to check
- `--fix` (optional): Automatically fix inconsistencies
- `--recursive` (optional): Flag to process subdirectories

**Processing Logic**:
1. Extract metadata from files (EXIF for images, PDF properties, etc.)
2. Compare metadata values against filename components
3. Identify inconsistencies and mismatches
4. Optionally correct filenames or metadata to ensure consistency

**Outputs**:
- Report of metadata-filename consistency
- List of files with inconsistencies
- Log of automatic fixes (if enabled)

### Reporting Scripts

#### 1. `organisation_report_generator.py`

**Purpose**: Generate comprehensive reports on file organisation status across the system.

**Input Parameters**:
- `--root-dirs` (required): List of directories to analyse
- `--report-type` (required): Type of report (compliance, structure, size, etc.)
- `--output-format` (optional): Format for report (PDF, HTML, JSON)
- `--include-charts` (optional): Flag to include visualisations in report

**Processing Logic**:
1. Traverse directory structure
2. Collect statistics on file types, naming compliance, organisation patterns
3. Analyse trends and identify problem areas
4. Generate formatted report with sections for different metrics
5. Create visualisations of key statistics

**Outputs**:
- Comprehensive report in specified format
- Statistical summaries of file organisation status
- Visualisations (charts, graphs) of key metrics
- Recommendations for improving organisation

#### 2. `storage_analyser.py`

**Purpose**: Analyse storage usage and identify optimisation opportunities.

**Input Parameters**:
- `--source-dirs` (required): Directories to analyse
- `--group-by` (optional): How to group results (type, age, size, etc.)
- `--min-size` (optional): Minimum file size to include in analysis
- `--output-format` (optional): Format for analysis report

**Processing Logic**:
1. Scan directories and collect file information
2. Calculate storage usage by various groupings
3. Identify large, duplicate, or rarely accessed files
4. Generate optimisation recommendations

**Outputs**:
- Storage usage report
- Identification of largest files and directories
- Optimisation recommendations
- Visualisation of storage distribution

### Utility Scripts

#### 1. `config_manager.py`

**Purpose**: Manage configuration settings for FOMO Python scripts.

**Input Parameters**:
- `--action` (required): Action to perform (get, set, reset, list)
- `--key` (conditional): Configuration key to get/set
- `--value` (conditional): Value to set for configuration key
- `--export` (optional): Export configuration to specified file

**Processing Logic**:
1. Load configuration from standard location
2. Perform requested action (get/set configuration values)
3. Validate configuration integrity
4. Save updated configuration

**Outputs**:
- Updated configuration file
- Console output confirming changes
- Validation of configuration integrity

#### 2. `integration_helper.py`

**Purpose**: Facilitate integration between Python scripts and other FOMO components.

**Input Parameters**:
- `--mode` (required): Integration mode (hazel, shortcut, applescript)
- `--action` (required): Action to perform
- `--params` (conditional): Parameters for the action
- `--callback` (optional): Callback mechanism for returning results

**Processing Logic**:
1. Parse and validate input parameters
2. Translate between Python script ecosystem and target component
3. Execute requested action
4. Format results for callback mechanism

**Outputs**:
- Action results in format expected by calling component
- Log of integration operations
- Error reporting in consistent format

## Implementation Priorities

The Python scripts component will be implemented in phases, with the following priorities:

| Priority | Script | Rationale | Timeline |
|----------|--------|-----------|----------|
| 1 | compliance_validator.py | Enables assessment of current state and establishes baseline | Week 1-2 |
| 1 | bulk_rename.py | Provides immediate value for standardising existing files | Week 1-2 |
| 2 | organisation_report_generator.py | Enables ongoing monitoring of compliance | Week 3-4 |
| 2 | config_manager.py | Required for consistent configuration across scripts | Week 3-4 |
| 3 | date_standardiser.py | Enhances naming consistency | Week 5-6 |
| 3 | integration_helper.py | Enables integration with other components | Week 5-6 |
| 4 | metadata_validator.py | Adds additional consistency checking | Week 7-8 |
| 4 | storage_analyser.py | Provides optimisation opportunities | Week 7-8 |

## Integration Points

The Python Scripts component integrates with other FOMO components as follows:

### Integration with Hazel Rules

| Script | Integration Method | Purpose |
|--------|-------------------|---------|
| bulk_rename.py | Command-line execution from Hazel | Triggered by Hazel when files are added to watched folders |
| compliance_validator.py | Results processing by Hazel | Hazel takes action based on compliance status |
| date_standardiser.py | Pre-processing for Hazel | Prepares files for further processing by Hazel rules |

### Integration with Apple Shortcuts

| Script | Integration Method | Purpose |
|--------|-------------------|---------|
| organisation_report_generator.py | Shortcut parameter passing | Generate reports on demand via Shortcuts |
| bulk_rename.py | File/folder selection via Shortcuts | Allow user to select files for bulk renaming |
| config_manager.py | Preferences management | Modify script behaviour through user-friendly interface |

### Integration with AppleScript Scripts

| Script | Integration Method | Purpose |
|--------|-------------------|---------|
| integration_helper.py | Bridge between Python and AppleScript | Facilitate bidirectional communication |
| metadata_validator.py | Data exchange | Share metadata validation results with AppleScript workflows |
| storage_analyser.py | Triggering mechanism | AppleScript can schedule and execute storage analysis |

## Version Control and Maintenance

All Python scripts will be maintained in a version control system with the following guidelines:

1. Scripts should be developed following PEP 8 style guidelines
2. Each script must include comprehensive docstrings and comments
3. Unit tests must be provided for core functionality
4. Scripts should log operations at appropriate detail levels
5. All scripts should implement proper error handling and user feedback
6. Configuration should be separated from code
7. Regular code reviews will be conducted to ensure quality and consistency

Scripts will be updated as file organisation requirements evolve, with backward compatibility maintained where possible.

