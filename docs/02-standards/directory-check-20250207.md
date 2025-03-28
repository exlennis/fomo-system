# System Directory Check
Last verified: 2025-02-07

## Key Directories:
* Home Directory: `/Users/ez`
* iCloud Drive: `/Users/ez/Library/CloudStorage`
* Dropbox:`/Users/ez/Library/CloudStorage/Dropbox-Personal`
* Google Drive: `/Users/ez/Library/CloudStorage/GoogleDrive`

## Document Directories:
* Documents: `/Users/ez/Documents`

## Project Directories:
* Design Projects: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-PROJECTS-`
* Dev Projects: `/Users/ez/Projects-Dev`

## Media Directories:
* Media (network shares): `/Volumes/∆Media`

## Working Directories:
* Design Assets: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-DESIGN-`
* Finance: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-FINANCE-`
* Work: `/Users/ez/Library/CloudStorage/Dropbox-Personal/-WORK-`
* Admin: `/Users/ez/Library/CloudStorage/Dropbox-Personal/admin`


---


# Folder Structure Core           # 2025-01-31

## MacBook Pro (Primary)          # 926GB (271GB free)
```markdown
├── Users/
│   └── ez/                     # Admin
│       ├── Documents/          # Synced via iCloud Drive
│       ├── Desktop/            # Synced via iCloud Drive
│       ├── Projects-Dev/       # Local development directory !!rename!!
│       └── Library/
│           ├── CloudStorage/   # location for cloud services
│           │   ├── Dropbox-Personal/
│           │   └── GoogleDrive-exlennis@gmail.com/
│           └── Mobile Documents/
│               └── com~apple~CloudDocs/  # iCloud Drive root
└── Volumes/
    ├── Macintosh HD -> /       # System link
    └── Macintosh HD-1          # Split system volume


## Mac Mini (Secondary)
├── Network Storage             # SMB shares
│   └── server/                 # File share
│   ├── ∆Media/                 # Media share
└── Shared Services
    ├── TM-Server/              # Network Time Machine backup
    ├── TM-MacBook/             # Network Time Machine backup
    └── ContentCaching/         # System service volume


## Cloud Storage
├── iCloud Drive                # ~/Library/Mobile Documents
│   ├── Desktop & Documents     # Using improved sync
│   ├── Downloads/              # Cloud download
│   └── Mobile Documents        # App-specific data
├── Dropbox                     # ~/Library/CloudStorage/Dropbox-Personal
└── Google Drive                # ~/Library/CloudStorage/GoogleDrive...
```


---


# Directory Tree

## Table of Contents
- [Core Folder Structure](#core-folder-structure)
- [Appendix A: Documents Folder Breakdown](#appendix-a-documents-folder-breakdown)
- [Appendix B: Media Directory Breakdown](#appendix-b-media-directory-breakdown)
- [Appendix C: Dropbox Folder Breakdown](#appendix-c-dropbox-folder-breakdown)
- [Appendix D: Working Directories](#appendix-d-working-directories)
- [Appendix E: Folder Automation Rules](#appendix-e-folder-automation-rules)

## Core Folder Structure

### Home Directory
```
/Users/ez
├── Applications
├── Desktop
├── Documents
├── Downloads
├── Library
├── Movies
├── Music
├── Pictures
├── Projects-Dev
└── Public
```

### iCloud Drive
```
/Users/ez/Library/CloudStorage
├── Dropbox-Personal
├── GoogleDrive
└── Mobile Documents
```

### Document Directories
```
/Users/ez/Documents
```

### Project Directories
```
/Users/ez/Library/CloudStorage/Dropbox-Personal/-PROJECTS-
/Users/ez/Projects-Dev
```

### Media Directories
```
/Volumes/∆Media
```

### Working Directories
```
/Users/ez/Library/CloudStorage/Dropbox-Personal/-DESIGN-
/Users/ez/Library/CloudStorage/Dropbox-Personal/-FINANCE-
/Users/ez/Library/CloudStorage/Dropbox-Personal/-WORK-
/Users/ez/Library/CloudStorage/Dropbox-Personal/admin
```

---

## Appendix A: Documents Folder Breakdown

### Documents Folder Breakdown
```
/Users/ez/Documents
├── FAMILY
│   ├── Asset Records
│   ├── Family Records
│   ├── Legal & Estate
│   ├── Visa Applications
│   └── Archive
├── FINANCE
│   ├── Banking
│   ├── Budgets
│   ├── Income & Expenses
│   ├── Insurance
│   ├── Investments
│   └── Taxes
├── PERSONAL
│   ├── Entertainment
│   ├── Health & Fitness
│   ├── Shopping & Food
│   ├── Tech
│   └── Travel
├── Admin
│   ├── FOMO
│   ├── App Support
│   ├── Automation Workflows
│   ├── Backup Strategy
│   └── Sync Fixes
└── Inbox
```

---

## Appendix B: Media Directory Breakdown

### Media Directory Breakdown
```
/Volumes/∆Media
├── Adult
├── Books
├── Movies
├── Music
├── TV Shows
└── Unsorted
```

---

## Appendix C: Dropbox Folder Breakdown

### Dropbox Folder Breakdown
```
/Users/ez/Library/CloudStorage/Dropbox-Personal
├── DESIGN
│   ├── Assets
│   ├── Docs
│   ├── Resources
├── FINANCE
│   ├── Banking
│   ├── Budgets
│   ├── Insurance
│   ├── Investments
│   └── Tax
├── PROJECTS
│   ├── Client Projects
│   ├── Internal Projects
│   ├── Designworks
│   ├── Studio Worldwide
│   ├── Development
│   └── Archive
└── WORK
```

---

## Appendix D: Working Directories

### Working Directories
```
/Users/ez/Library/CloudStorage/Dropbox-Personal
├── -DESIGN-
├── -FINANCE-
├── -WORK-
├── -ADMIN-
└── -PROJECTS-
```

---

## Appendix E: Folder Automation Rules

### Folder Automation Rules
- **Downloads Folder** (TBC): Auto-sorts files into **Design, Finance, Work, and Personal** categories.
- **Inbox Folder** (TBC): Temporary holding area for unsorted files, with an auto-cleanup rule.
- **Archive Folder**: Automatically moves inactive files older than six months.
- **Smart Folders Using Tags** (TBC): Implementing tag-based Smart Folders for dynamic file organisation.
