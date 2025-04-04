# Apple Shortcuts Overview Draft (for reference only)

## Table of Contents
- [Overview](#overview)
- [Shortcut Categories](#shortcut-categories)
- [Shortcut Definitions](#shortcut-definitions)
- [Implementation Priorities](#implementation-priorities)
- [Integration Points](#integration-points)
- [Next Steps](#next-steps)

## Overview

This document provides comprehensive specifications for Apple Shortcuts to be implemented as part of the FOMO (File Organisation, Management & Optimisation) system. Apple Shortcuts will serve as user-facing automation interfaces that enable quick access to file operations, search functions, and trigger points for other FOMO components.

## Shortcut Categories

Apple Shortcuts for the FOMO system are organised into the following categories:

| Category | Description | Primary Use Cases |
|----------|-------------|-------------------|
| File Access | Shortcuts that provide quick access to commonly used files and folders | Opening Smart Folders, recent documents, project folders |
| Search Operations | Shortcuts that facilitate enhanced file search capabilities | Finding files by metadata, content search, date-based queries |
| Automation Triggers | Shortcuts that initiate automated workflows | Starting batch processing, initiating compliance checks |
| File Operations | Shortcuts that perform direct file manipulation | Renaming, moving, tagging files |
| System Integration | Shortcuts that connect FOMO with other system components | Linking with Raycast, Terminal, Finder |

## Shortcut Definitions

### File Access Shortcuts

#### Smart Folder Access

| Attribute | Specification |
|-----------|---------------|
| Name | Smart Folder Quick Access |
| Description | Opens predefined Smart Folders with a single command |
| Trigger | Voice command, keyboard shortcut, or Raycast integration |
| Actions | 1. Present menu of available Smart Folders<br>2. Open selected Smart Folder in Finder |
| Outputs | Opened Smart Folder window |
| Variables | List of Smart Folder paths |
| Error Handling | Alert if Smart Folder cannot be found |

#### Recent Projects

| Attribute | Specification |
|-----------|---------------|
| Name | Recent Projects Navigator |
| Description | Provides quick access to recently accessed project folders |
| Trigger | Keyboard shortcut or Raycast command |
| Actions | 1. Generate list of recently accessed project folders<br>2. Present menu for selection<br>3. Open selected folder |
| Outputs | Opened project folder |
| Variables | Number of recent items to display (default: 10) |
| Error Handling | Fallback to manual folder selection if history unavailable |

### Search Operations Shortcuts

#### Metadata Search

| Attribute | Specification |
|-----------|---------------|
| Name | Metadata Search Tool |
| Description | Search files across the system based on metadata attributes |
| Trigger | Keyboard shortcut or menu option |
| Actions | 1. Present search form with metadata fields<br>2. Construct search query<br>3. Execute search<br>4. Present results in sortable list |
| Outputs | List of matching files with action options |
| Variables | Search fields, locations to search, result limit |
| Error Handling | Provide suggestions if no results found |

#### Date-Based File Finder

| Attribute | Specification |
|-----------|---------------|
| Name | Date-Based File Finder |
| Description | Locate files modified or created within specific date ranges |
| Trigger | Voice command or keyboard shortcut |
| Actions | 1. Present date range selector<br>2. Construct date query<br>3. Execute search<br>4. Present results chronologically |
| Outputs | Chronological list of files with preview capability |
| Variables | Date range (Today, This Week, Custom) |
| Error Handling | Option to expand search parameters if no results |

### Automation Trigger Shortcuts

#### Batch Processing Initiator

| Attribute | Specification |
|-----------|---------------|
| Name | Batch Processing Initiator |
| Description | Triggers batch processing workflows for selected files or folders |
| Trigger | Context menu or keyboard shortcut |
| Actions | 1. Accept file selection or folder path<br>2. Present processing options (rename, optimise, validate)<br>3. Initiate selected workflow<br>4. Monitor and report progress |
| Outputs | Progress indication and completion report |
| Variables | Processing type, target files/folders |
| Error Handling | Pause/resume capability for large batches |

#### Compliance Check Trigger

| Attribute | Specification |
|-----------|---------------|
| Name | Naming Compliance Checker |
| Description | Initiates verification of file naming standards compliance |
| Trigger | Manual execution or scheduled trigger |
| Actions | 1. Select target directory<br>2. Initiate Python compliance script<br>3. Collect and format results<br>4. Present compliance report |
| Outputs | Compliance summary with actionable recommendations |
| Variables | Target directory, ruleset to check against |
| Error Handling | Detailed logging of verification failures |

### File Operations Shortcuts

#### Structured Renaming Tool

| Attribute | Specification |
|-----------|---------------|
| Name | Structured Renaming Tool |
| Description | Rename files according to FOMO naming conventions |
| Trigger | Context menu on file selection |
| Actions | 1. Extract file metadata<br>2. Present naming template options<br>3. Generate preview of new names<br>4. Execute renaming operations |
| Outputs | Renamed files and confirmation summary |
| Variables | Naming templates, metadata extraction rules |
| Error Handling | Conflict resolution for duplicate names |

#### Bulk Tag Manager

| Attribute | Specification |
|-----------|---------------|
| Name | Bulk Tag Manager |
| Description | Apply, remove, or modify tags across multiple files |
| Trigger | Keyboard shortcut or context menu |
| Actions | 1. Select files for tag operations<br>2. Present tag manipulation interface<br>3. Preview changes<br>4. Apply tag modifications |
| Outputs | Updated file tags and operation summary |
| Variables | Tag presets, selection rules |
| Error Handling | Verification step before applying changes |

### System Integration Shortcuts

#### Raycast Command Bridge

| Attribute | Specification |
|-----------|---------------|
| Name | FOMO Raycast Bridge |
| Description | Expose FOMO functionality through Raycast commands |
| Trigger | Raycast command palette |
| Actions | 1. Register FOMO commands in Raycast<br>2. Provide parameter interfaces<br>3. Execute corresponding shortcut<br>4. Return results to Raycast UI |
| Outputs | Command execution and visual feedback in Raycast |
| Variables | Command list, parameter definitions |
| Error Handling | Graceful error reporting within Raycast interface |

#### Terminal Workflow Initiator

| Attribute | Specification |
|-----------|---------------|
| Name | Terminal Workflow Initiator |
| Description | Launch terminal-based FOMO workflows from shortcuts |
| Trigger | Keyboard shortcut or menu selection |
| Actions | 1. Present workflow selection menu<br>2. Configure workflow parameters<br>3. Generate and execute terminal commands<br>4. Capture and present output |
| Outputs | Terminal execution results formatted for user consumption |
| Variables | Available workflows, parameter templates |
| Error Handling | Command validation before execution |

## Implementation Priorities

Implementation of Apple Shortcuts for the FOMO system will follow these priorities:

| Priority | Shortcut | Rationale | Estimated Complexity |
|----------|----------|-----------|----------------------|
| 1 | Smart Folder Quick Access | Provides immediate value with minimal development effort | Low |
| 2 | Structured Renaming Tool | Addresses core file organisation need | Medium |
| 3 | Metadata Search Tool | Enhances findability, a key FOMO objective | Medium |
| 4 | Batch Processing Initiator | Enables scaling of file operations | High |
| 5 | FOMO Raycast Bridge | Improves system accessibility | Medium |
| 6 | Compliance Check Trigger | Supports governance objectives | Medium |
| 7 | Recent Projects Navigator | Enhances user workflow | Low |
| 8 | Date-Based File Finder | Complements search capabilities | Medium |
| 9 | Bulk Tag Manager | Extends organisational capabilities | Medium |
| 10 | Terminal Workflow Initiator | Provides advanced user functionality | High |

## Integration Points

Apple Shortcuts will integrate with other FOMO components as follows:

| FOMO Component | Integration Method | Data Exchange | Triggers |
|----------------|---------------------|---------------|----------|
| Hazel Rules | Direct folder access, status checking | Folder paths, rule status | Can initiate Hazel processing by placing files in watched folders |
| Python Scripts | Shell script action, parameters passing | Command-line arguments, JSON data exchange | Direct execution with parameters |
| AppleScript Scripts | Direct AppleScript execution | Variable passing, return values | Function calls with context |
| File System | Finder integration, file actions | File paths, metadata | File operations trigger events |
| Raycast | Custom commands registration | Command parameters, results | User-initiated commands |
| System Services | URL schemes, x-callback-url | Structured data payloads | Cross-application automation |

### Integration Diagram

The integration between Apple Shortcuts and other components follows this general pattern:

1. User initiates shortcut via keyboard, voice, or Raycast
2. Shortcut performs preliminary actions (gather input, validate)
3. Shortcut triggers appropriate component:
   - Executes Python script with parameters
   - Runs AppleScript with context
   - Places files in Hazel-monitored location
   - Performs direct file system operations
4. Shortcut captures results and presents to user
5. (Optional) Shortcut initiates follow-up actions based on results

## Next Steps

To proceed with implementation of the Apple Shortcuts component:

1. Validate shortcut specifications with stakeholders
2. Create prototype of highest priority shortcuts
3. Establish testing methodology for shortcuts
4. Develop shortcut templates to ensure consistency
5. Document shortcut usage for end-users
6. Integrate with other FOMO components as they are developed
7. Establish update and maintenance protocols

Implementation should follow an iterative approach, starting with core functionality and expanding as the system matures.

---

*This specification is subject to revision as the FOMO system development progresses. All shortcuts should be tested in isolation before integration with other system components.*

