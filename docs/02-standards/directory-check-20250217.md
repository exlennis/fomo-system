# System Directory Check
Last verified: 2025-02-17


## Tree Structure

```

=== User Home Directory ===
/Users/ez/
├── Desktop/                          # ✓ [700] iCloud Sync Enabled
├── Documents/                        # ✓ [700] iCloud Sync Enabled
├── Downloads/                        # ✓ [750] Local Downloads Folder
└── Local/                            # ✓ [755]
    └── -PROJECTS-Dev/                # ✓ [750] Development Projects


=== Cloud Storage Directory ===
/Users/ez/Library/CloudStorage/
├── iCloud Drive/                     # ✓ [750]
│   ├── Desktop/                      # ✓ [750] Sync with ~/Desktop
│   ├── Documents/                    # ✓ [750] Sync with ~/Documents
│   │   ├── -PERSONAL-/               # ✓ [700]
│   │   ├── -FAMILY-/                 # ✓ [700]
│   │   └── -FINANCE-/                # ✓ [750]
│   ├── Downloads+/                   # ✓ [700] iCloud Downloads Folder
│   └── Notes/                        # ✓ [750] Synced Obsidian Valuts
├── Dropbox/                          # ✓ [750]
│   ├── -PROJECTS-/                   # ✓ [750] Design Projects
│   ├── -WORK-/                       # ✓ [750]
│   └── -DESIGN-/                     # ✓ [750] Creative Assets
└── GoogleDrive/                      # ✓ [500] Restricted Access


=== Network Shares & External Volumes ===
/Volumes/
├── Macintosh HD/                     # ✓ [755] System Volume
├── Data/                             # ✓ [755] User Data Volume
└── ∆Media/                           # ? Mount status pending verification

```

## Status Report

### User Home
- Path: `/Users/ez`
- Permissions: 750
- Status: Verified

### Mobile Documents
Parent directory containing CloudDocs and other cloud-synced app data
- Path: `/Users/ez/Library/Mobile Documents`
- Permissions: 500
- Status: Verified

### iCloud Drive
- Path: `/Users/ez/Library/Mobile Documents/com~apple~CloudDocs`
- Permissions: 700
- Status: Verified

### iCloud Drive Base
- Path: `/Users/ez/Library/CloudStorage`
- Permissions: 750
- Status: Verified

### Dropbox
- Path: `/Users/ez/Library/CloudStorage/Dropbox-Personal`
- Permissions: 750
- Status: Verified

### Google Drive
- Path: `/Users/ez/Library/CloudStorage/GoogleDrive-exlennis@gmail.com`
- Permissions: 500
- Status: Verified

### Media
External hard drive or network share - mount status pending
- Path: `/Volumes/∆Media`
- Permissions: N/A
- Owner: N/A (Unexpected)
- Status: === UNABLE TO VERIFY ===

### Notes (Obsidian)
Markdown notes in Obsidian vault
- Path: `/Users/ez/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes`
- Permissions: 700
- Status: Verified

## Key Directories

### Desktop
Synced via iCloud Drive
- Local path: `/Users/ez/Desktop`
- iCloud path: `/Users/ez/Library/Mobile Documents/com~apple~CloudDocs/Desktop`
- Permissions: 700
- Status: Verified

### Documents
Synced via iCloud Drive
- Local path: `/Users/ez/Documents`
- iCloud path: `/Users/ez/Library/Mobile Documents/com~apple~CloudDocs/Documents`
- Permissions: 700
- Status: Verified

### Downloads 
Local Downloads folder (not in use, use iCloud instead)
- Path: `/Users/ez/Downloads`
- Permissions: 750
- Status: Verified

### Downloads+ (iCloud)
- Path: `/Users/ez/Library/Mobile Documents/com~apple~CloudDocs/Downloads+`
- Permissions: 700
- Status: Verified

### Local
Local folder for admin and system files
- Path: `/Users/ez/Local`
- Permissions: 755
- Status: Verified

### Projects-Design
- Path: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-PROJECTS-`
- Permissions: 750
- Status: Verified

### Projects-Dev
- Path: `/Users/ez/Local/-PROJECTS-`
- Permissions: 750
- Status: Verified

### Work
- Path: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-WORK-`
- Permissions: 750
- Status: Verified

### Knowledge
To be renamed 'Knowledge' to better reflect scope change
- Path: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-DESIGN-`
- Permissions: 750
- Status: Verified

### Personal
- Path: `/Users/ez/Documents/-PERSONAL-`
- Permissions: 700
- Status: Verified

### Family
- Path: `/Users/ez/Documents/-FAMILY-`
- Permissions: 700
- Status: Verified

### Finance
- Path: `/Users/ez/Documents/-FINANCE-`
- Permissions: 750
- Status: Verified

## Notable findings:
- 21 of 22 critical directories are verified and accessible.
- All verified directories are owned by user 'ez'.
- All verified directories have appropriate permissions (700-755).
- Unable to verify path (may be due to mounted volumes or cloud service configurations) for the following directories:
  - Media

