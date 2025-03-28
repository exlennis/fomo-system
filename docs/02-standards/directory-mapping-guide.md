# Directory Mapping and Verificaiton Guide

*About this document:*
- **Contains**: Specific directory paths and their purposes in the system
- **Primary focus**: Documentation of system directories, their locations and purposes
- **Purpose**: Provide a verified map of important system directories
- **Key components**: Directory paths, purpose descriptions, verification status, path migration notes
- **Last verified:** 2025-02-17

## Key System Directories

### Home Directory
```
/Users/ez
```

### Standard User Directories
- Desktop (iCloud synced): `/Users/ez/Desktop`
- Documents (iCloud synced): `/Users/ez/Documents`

## Cloud Storage Locations

### iCloud Drive
Base directory:
```
/Users/ez/Library/CloudStorage
```

Active files location:
```
/Users/ez/Library/Mobile Documents/com~apple~CloudDocs
```
- Primary location for iCloud Drive files
- Contains synced Desktop and Documents

### Dropbox
```
/Users/ez/Library/CloudStorage/Dropbox-Personal
```

### Google Drive
```
/Users/ez/Library/CloudStorage/GoogleDrive
```

## Administrative Directories

### Admin Resources
- Local Admin: `/Users/ez/Local` (moved from Dropbox)
- Downloads:
- Local Downloads: [Path to be verified]
- Downloads+ (iCloud): [Path to be verified]
- Notes (Obsidian): [Path to be verified]

### Work Resources
- Work Directory: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-WORK-`
- Design Projects: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-PROJECTS-`
- Development Projects: `/Users/ez/Local/-PROJECTS-` (moved from Projects-Dev)
- Knowledge Base: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-DESIGN-` (considering rename to KNOWLEDGE)

### Personal Resources
- Finance: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-FINANCE-`
- Family: [Path to be verified]
- Media: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-MEDIA-`

### External Media
```
/Volumes/∆Media
```
Status: Currently not mounted (unable to verify)

## Important Notes
1. Several directories have been relocated:
- Admin directory moved to `/Users/ez/Local`
- Projects-Dev renamed and moved to `/Users/ez/Local/-PROJECTS-`
- Finance directory remains in Dropbox

2. Sync Status:
- Desktop and Documents are synced through iCloud
- Work and Design directories are managed through Dropbox
- Development projects moved to Local storage

3. Pending Verifications:
- Some paths need verification (marked with [Path to be verified])
- External media volume currently unmounted
- Knowledge Base rename proposal under consideration

## Verification Method
This information was verified using direct system checks on 2025-02-17. Commands used:
```bash
# Directory verification
ls -d /Users/ez/Library/CloudStorage/*
ls -d /Users/ez/Library/Mobile\ Documents/com~apple~CloudDocs
ls -d ~/Local
ls -d ~/Desktop
ls -d ~/Documents
```

## Overview
This document outlines the key directory paths related to iCloud Drive and CloudStorage on macOS, verified through direct system checks.

## Directory Paths

### CloudStorage Base Directory
```
/Users/ez/Library/CloudStorage
```
- Purpose: Storage location for cloud-synced application data
- Used by applications for storing cloud-synced configurations and data

### Main iCloud Drive (CloudDocs) Directory
```
/Users/ez/Library/Mobile Documents/com~apple~CloudDocs
```
- This is where your actual iCloud Drive files are stored
- Directory permissions: drwx------ (user-only access)
- Owner: ez
- Group: staff

### Mobile Documents Directory
```
/Users/ez/Library/Mobile Documents/
```
- Parent directory containing CloudDocs
- Houses other cloud-synced app data
- Contains the com~apple~CloudDocs directory

## Important Notes
- The CloudStorage directory (/Library/CloudStorage) is specifically for application data and should not be confused with the main iCloud Drive location
- The actual iCloud Drive content is stored in the com~apple~CloudDocs directory
- These paths are current as of macOS latest versions and may be subject to change in future updates

## Verification Method
This information was verified using direct system checks:
```bash
echo "=== iCloud Related Paths ==="
echo "CloudStorage: ~/Library/CloudStorage"
echo "iCloud Drive (CloudDocs): $(ls -d ~/Library/Mobile Documents/com~apple~CloudDocs)"
ls -la ~/Library/Mobile Documents/com~apple~CloudDocs/.. | grep "CloudDocs"
```
