# FOMO Directory Architecture: Multi-Machine Implementation

Based on the current setup, file flow diagrams, and pain points, We've developed a comprehensive directory structure optimisation plan focused on your top-level architecture priorities. The design aims to balance logical organization with your existing cloud workflow while minimising disruption.


### Key Stats Overview:

- **8x symlinks** in total pointed from cloud storage to local directories in the home folders
- **2x symlinks** already exist, namely `iCloud/Desktop` and `iCloud/Documents`
- Additional **2x iCloud symlinks** and **4x Dropbox symlinks** need to be created
- A total of **4x new folders** will be created at the base level of the home directory
- **4x backups** need to be set up, ensuring all information is either coming from the cloud or backed up

### Naming Conventions:

- Any restructuring work, such as folder renaming, must be completed first in all cloud locations before working on local folders
- Taking this restructuring opportunity at a system level, we encourage correcting any folder names that do not follow the FOMO standards
- Specifically: Level 1 folders should be standardised as one-word letters with capitalisation, following the macOS home folder naming convention
- Any other nested folders should use all lowercase with hyphens as separators
- Exceptions are made for top-level project and client folders, and domain-specific edge cases



## 1. Complete Directory Mapping

Your main issues stem from excessive folder depth, scattered resources, and inconsistent naming. Here's a comprehensive mapping showing both physical locations and logical structure that addresses these problems while maintaining your cloud sync requirements:


#### **Network Attached Storage**
```
Media/                                    # renamed from /Volumes/∆Media
├─── Books/                               # Calibre managed library
│    ├─── inbox/                          # renamed from -Unsorted-Books
│    ├─── Frank Herbert
│    └─── ... (other authors)
├─── Movies/                              # Plex managed library
│    ├─── inbox/                          # renamed from -Unsorted-Movies
│    ├─── A Star Is Born (2018)/
│    └─── ... (other movies)
├─── Music/                               # Plex managed library
│    ├─── inbox/                          # renamed from -Unsorted-Musics
│    ├─── Chinese Music/
│    └─── ... (other music)
├─── Photos/                              # Plex managed library
│    ├─── inbox/                          # renamed from -Unsorted-Photos
│    ├─── 2012/
│    └─── ... (other photos)
├─── Restricted/                          # renamed Jellyfin managed library 
│    ├─── inbox/                          # renamed
│    ├─── R-Studios/
│    └─── ... (other content)
└─── Shows/                               # renamed from TV Shows, Plex managed library
     ├─── inbox/                          # renamed from -Unsorted-tvShows
     ├─── American Horror Story (2011)/
     └─── ... (other TV shows)

│L0..│L1..│L2..│
```


#### **Cloud Storage**
```
Dropbox/
│••• Design/ ••••••••••••••••••••••••••••• # Remove to reduce folder level, simplify structure
│••• Work/                                 # Relocate to /iCloud/Documents/work/
│                          Thinking Ahead: # Plan use home server or NAS, backup using Time Machine or Git 
│                                          
├─── Docs/ ── ── ── ── ── ── ── ── ── ──>> # Keep existing structure, symlink to ~/Knowledge/docs/
├─── Reference/─ ── ── ── ── ── ── ── ──>> # Renamed from Resources, symlink to ~/Resources/reference/
├─── Assets/── ── ── ── ── ── ── ── ── ─>> # Keep existing structure, symlink to ~/Resources/assets/
│    ├─── assets-coll/
│    ├─── fonts/
│    ├─── icons/
│    ├─── colours/
│    ├─── wallpapers/
│    └─── ...              Thinking Ahead: # Only design projects left, reducing storage plan significantly        
└─── Projects/ ─────────────────────────>> # Renamed from -PROJECTS-, symlink to ~/Projects/design/
     ├─── 10 Personal/       
     ├─── 15 Self-titled/               
     └─── ...

iCloud Drive/
├─── Desktop/ ──────────────────>> EXISTING: Symlink ~/Desktop/  
├─── Documents/ ────────────────>> EXISTING: Symlink ~/Documents/                       
│    ├─── personal/                        # Renamed from -Personal-
│    ├─── family/                          # Renamed from -Family-
│    ├─── finance/                         # Renamed from -Finance-
│    ├─── work/                            # Relocated from /Dropbox/Work/ (work-related documents)
│    │    ├─── career/                   
│    │    ├─── education/
│    │    ├─── employment/
│    │    └─── ...
├─── Downloads/ ────────────────────────>> # Renamed from Downloads+, symlinks to ~/Downloads/
│    ├─── inbox/                           # New structure
│    ├─── processing/
│    └─── archive/
└─── Obsidian/ ─────────────────────────>> # Keep existing structure, symlink to ~/Knowledge/vault/
     ├─── notes/
     ├─── archive/
     └─── attachments/                      


│L0..│L1..│L2..│
```


#### Logical Access Structure
```
~/                                        # Home directory
├─── Resources/                           # Container for all supportive materials
│    ├─── assets/ <<─────────────────────── ~/…/Dropbox-Personal/Assets/
│    │    ├─── assets-coll/               # Eagle managed Collection of design assets
│    │    ├─── fonts/
│    │    ├─── icons/ 
│    │    ├─── colours/ 
│    │    ├─── wallpapers/
│    │    └─── ...     
│    ├─── catalogues/                     # Organisation systems for resources  ──────────────────────────────> TimeMachine backup 
│    │    ├─── TagSpaces-meta/            # Asset management app metadata
│    │    ├─── RightFont-meta/            # Font app metadata
│    │    ├─── prompt-cat/ 
│    │    └─── ...            
│    ├─── reference/ <<──────────────────── ~/…/Dropbox-Personal/Resources/ (information consulted but rarely modified)
│    └─── templates/                      # Starting points for new work moving ~/Local/templates/ ───────────> Git backup
├─── Projects/                            # Unified project access (work actively creating)
│    ├─── dev/                            # Relocate ~/Local/-PROJECTS-Dev/ ──────────────────────────────────> Git backup
│    └─── design/ <<─────────────────────── Dropbox/projects/
├─── Knowledge/                           # Knowledge management (Information collected or created)
│    ├─── vault/ <<──────────────────────── ~/…/iCloud~md~obsidian/Documents/ (Local PKM markdown based)
│    └─── docs/ <<───────────────────────── ~/…/Dropbox-Personal/Docs/ (PDFs and other docs)
├─── System/                              # Computer management and configuration renamed ~/Local/ ───────────> Git backup
│    ├─── configs/                        # Application configs
│    ├─── scripts/                        # Automation scripts
│    └─── search/                         # Saved searches, smart folders & queries
├─── Downloads/ <<───────────────────────── ~/…/com~apple~CloudDocs/Downloads/
├─── Desktop/ <<───────────────── EXISTING: Symlink /iCloud/Desktop/
├─── Documents/ <<─────────────── EXISTING: Symlink /iCloud/Documents/
│    ├─── work/                           # ~/…/Dropbox-Personal/work/ relocated 
│    ├─── personal/   
│    ├─── family/                         
│    └─── finance/                  
└─── ...

│L0..│L1..│L2..│
```

### A Better High-Level Organisation

1. **Reduced Path Depth**: Creates logical groupings at the top level
2. **Centralised Resources**: Consolidates scattered assets through symlinks
3. **Clear Purpose Separation**: Each top-level directory has a distinct function
4. **Maintains Cloud Sync**: Uses symlinks to preserve cloud storage benefits

```
~/                                        # Home directory
├─── Applications/                        # in Alphabetical order
├─── Desktop/                             # Transient files
├─── Documents/                           # Documents (Personal, Family, Finance & Work)
├─── Downloads/                           # Automated processing
├─── Knowledge/ <<──────────────────── NEW: Information collected or created 
├─── Library/
├─── Movies/
├─── Music/
├─── Pictures/
├─── Projects/ <<───────────────────── NEW: Centralised work hub for working/creating 
├─── Public/                            
├─── Resources/ <<──────────────────── NEW: Materials that support work
└─── System/ <<─────────────────────── NEW: Computer management and configuration

│L0..│L1..│
```


## 2. Implementation Strategy

### 2.1 Physical to Logical Mapping

The structure above uses symlinks to create a logical organisation while preserving your physical storage locations:

| Logical Path | Physical Location | 
|--------------|-------------------|
| ~/Resources/assets/ | → /Users/ez/Library/CloudStorage/Dropbox-Personal/-DESIGN-/Assets/ |
| ~/Resources/templates/ | → Multiple locations consolidated |
| ~/Projects/dev/ | → /Users/ez/Local/-PROJECTS-Dev/ |
| ~/Projects/design/ | → /Users/ez/Library/CloudStorage/Dropbox-Personal/-PROJECTS-/ |
| ~/Knowledge/vault/ | → /Users/ez/Library/iCloud~md~obsidian/Documents/Notes |


### 2.2 CLI Navigation Enhancement

To solve your CLI navigation issues with deep paths:

```bash
# Add to your .zshrc or equivalent
# Quick navigation to major areas
alias res="cd ~/Resources"
alias proj="cd ~/Projects"
alias pdev="cd ~/Projects/dev"
alias pdes="cd ~/Projects/design"
alias know="cd ~/Knowledge"
alias dl="cd ~/Downloads+"

# Smart project jumping
proj() {
  local base="$HOME/Projects"
  if [ -z "$1" ]; then
    cd "$base"
  else
    local target=$(find "$base" -maxdepth 2 -type d -name "*$1*" | head -1)
    if [ -n "$target" ]; then
      cd "$target"
    else
      echo "No matching project found."
    fi
  fi
}
```

### 2.3 Multi-Machine Setup 

This setup can be effectively replicated across multiple machines. 

Recommended Approach:
- **Use `$HOME` variable**: Absolutely correct - using `$HOME` instead of hardcoded `/Users/ez/` makes the script portable.
- **Machine detection**: Add a simple hostname check to apply machine-specific configurations.
- **Relative paths**: For symlinks, absolute paths are generally more reliable, but using variables makes them portable.


### 2.4 Setup Script for Multiple Machines


This script creates the necessary directory structure and symlinks:

```bash
#!/bin/bash
# fomo-directory-setup.sh

# Determine machine type for machine-specific settings
HOSTNAME=$(hostname)
case "$HOSTNAME" in
  "MacMini"*)
    MACHINE_TYPE="server"
    ;;
  "Work"*)
    MACHINE_TYPE="work"
    ;;
  *)
    MACHINE_TYPE="personal"
    ;;
esac

# Set base paths (adjust if needed per machine)
DROPBOX_PATH="$HOME/Library/CloudStorage/Dropbox-Personal"
ICLOUD_PATH="$HOME/Library/CloudStorage/iCloud Drive"
OBSIDIAN_PATH="$HOME/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes"

# Create base directories
mkdir -p "$HOME/Resources"/{assets,templates,libraries,fonts}
mkdir -p "$HOME/Projects"/{dev,design}
mkdir -p "$HOME/Knowledge"/{vault,docs,reference}
mkdir -p "$HOME/System"/{configs,scripts}
mkdir -p "$HOME/Work"  # For work-related personal documents

# Set up symlinks based on machine type
echo "Setting up for $MACHINE_TYPE machine..."

# Common symlinks across all machines
ln -sf "$DROPBOX_PATH/design/Assets" "$HOME/Resources/assets"
ln -sf "$OBSIDIAN_PATH" "$HOME/Knowledge/vault"
ln -sf "$DROPBOX_PATH/design/Resources" "$HOME/Knowledge/reference"
ln -sf "$DROPBOX_PATH/projects" "$HOME/Projects/design"
ln -sf "$DROPBOX_PATH/work" "$HOME/Work"

# Machine-specific configurations
if [ "$MACHINE_TYPE" = "server" ]; then
  # Server-specific settings
  echo "Adding server-specific configurations..."
  # Add more server-specific symlinks here
elif [ "$MACHINE_TYPE" = "work" ]; then
  # Work machine settings
  echo "Adding work machine configurations..."
  # Potentially limit certain personal symlinks
else
  # Personal machine gets everything
  echo "Adding personal machine configurations..."
fi

echo "Directory structure created successfully for $MACHINE_TYPE!"
```


## Symlinks & Cloud Storage 

Your concerns about symlinks and cloud storage are valid, especially given your past experiences.

### Safe Implementation Guidelines

1. **Direction Matters**: Always point FROM cloud storage TO local organization
   ```bash
   # SAFE: Local pointer to cloud location
   ln -sf "$DROPBOX_PATH/design/Assets" "$HOME/Resources/assets"
   
   # AVOID: Cloud location pointing to another cloud location
   # ln -sf "$ICLOUD_PATH/something" "$DROPBOX_PATH/something-else"
   ```

2. **Never Create Bidirectional Links**: This avoids sync conflicts
   
3. **Test First**: Create one symlink and observe sync behavior for 24 hours before full implementation

### Network Considerations

- **Mac File Sharing**: Works well with symlinks within the same system
- **Tailscale/Tailnet**: No direct impact on symlinks; just affects network access
- **VPNs/iCloud Relay**: Minimal impact, may slightly affect sync speeds
- **Important**: If using Time Machine or other backups, ensure they follow symlinks correctly





### Library vs Asset Organization

The distinction is important:
- **Assets**: Actual design files you use (fonts, icons, photos)
- **Libraries**: Metadata, collections, organizational systems for those assets

For your specific questions:
- **Font files**: Physical files in `~/Resources/assets/fonts/` (pointing to Dropbox)
- **Font management**: Metadata in `~/Resources/libraries/font-collections/`
- **Mockups & stock photos**: Under `~/Resources/assets/` as they're design assets
- **Prompt library**: Under `~/Resources/libraries/prompt-collections/`
- **Script library**: Move to `~/System/scripts/` as they're system utilities

### Local Folder Considerations

- **Knowledge/docs**: This is for structured documentation you might want in Git or outside Obsidian. Examples include technical documentation, code docs, or project wikis.
- **Downloads**: You can symlink local Downloads to iCloud/Downloads+ for centralized management.
- **Local folder**: After migration, you can gradually refactor this, keeping only essential parts.



## 3. Naming Standards Framework

To address your naming consistency concerns:

### 3.1 Standardised Terms

| Concept | Standard Form | Never Use |
|---------|---------------|-----------|
| Template | `template` or `tpl` | `TPLP`, `templat` |
| Working | `working` (suffix) | `wip`, `work-in-progress` |
| Archive | `archive` (singular) | `archives`, `old` |
| GitHub | `github` (lowercase) | `GitHub`, `gh` |
| Configuration | `config` | `conf`, `cfg` |

### 3.2 Prefix/Suffix Standards

Always use consistent patterns:

- **State indicators**: Always as suffixes 
  - `logo-working.ai`, `document-approved.pdf`
- **Type indicators**: Always as prefixes
  - `tpl-invoice.docx`, `config-vscode.json`
- **Date stamps**: Always as prefixes with YYYYMMDD format
  - `20250310-meeting-notes.md`
- **Version numbers**: Always as suffixes with v## format
  - `proposal-v01.pdf`, `logo-v02.svg`

### 3.3 Capitalisation Rules

- **Directories**: All lowercase-kebab-case (`client-projects/`)
- **Files**: lowercase-kebab-case (`project-document.md`)
- **Project names**: Title case when used in content, lowercase in paths
- **Proper nouns**: Only capitalised in content, lowercase in file/directory names



## 4. Addressing Your Pain Points

### 4.1 Folder Depth Problem

1. **Shallower Structure**: The new architecture reduces required path depth 
2. **Logical Grouping**: Related resources are grouped by function
3. **CLI Navigation**: Shell aliases and functions make navigation faster
4. **Symbolic Links**: Create a logical structure decoupled from physical storage

### 4.2 Scattered Resources Solution

1. **Central Resources Hub**: All assets, templates, libraries in one logical location
2. **Physical Location Preservation**: Symlinks maintain cloud sync while providing unified access
3. **Standardised Access Patterns**: Consistent paths regardless of physical storage
4. **Application Integration**: Update applications to look in the new logical paths

### 4.3. Naming Consistency Framework

1. **Documented Standards**: Clear rules for abbreviations, prefixes/suffixes
2. **Implementation Guides**: Templates for common naming patterns
3. **Validation Tools**: Scripts to check compliance with naming standards
4. **Migration Path**: Gradual standardisation of existing files


### 5.1 Git & Knowledge Management

For your Obsidian concerns:

1. **Hybrid Approach**: Keep the vault in iCloud for accessibility
2. **Selective Git Integration**: Create a git repository within specific vault folders
3. **Gitignore Strategy**: Exclude attachments, images, and binary files from git
4. **GitHub Flexibility**: Git repositories can be located anywhere on your system and don't need to be in a single parent folder

### 5.2 Downloads Management

For your active Downloads+ area:

1. **Three-Stage Pipeline**:
   - `inbox/`: All new files land here
   - `processing/`: Files being sorted and renamed
   - `archive/`: Temporary storage for processed files
   
2. **Hazel Automation Rules**:
   - Type detection: Categorise by file type
   - Naming standardisation: Apply FOMO naming patterns
   - Destination routing: Move to appropriate final locations
   


## 6. Implementation Plan

### Phase 1: Setup and Testing (Days 1-2)
1. Create the new logical directory structure
2. Set up initial symlinks for most frequently accessed locations
3. Create shell aliases and functions for navigation
4. Test with a small subset of frequent tasks

### Phase 2: Resource Consolidation (Days 3-5)
1. Inventory all templates, assets, and libraries
2. Create appropriate symlinks in the Resources structure
3. Test application integration with new paths
4. Document physical-to-logical mappings

### Phase 3: Downloads Optimization (Days 6-7)
1. Set up three-stage pipeline in Downloads+
2. Create Hazel rules for automation
3. Test with common file types
4. Refine rules based on usage patterns

### Phase 4: Documentation and Training (Days 8-10)
1. Create comprehensive directory structure guide
2. Document naming standards and conventions
3. Create quick reference materials
4. Practice new workflows to build habits



## Benefits, Limitations & Maintenance

### Key Benefits
- **Unified Access**: Consistent paths regardless of physical storage
- **Reduced Complexity**: Shorter paths and logical grouping
- **Flexibility**: Adapts as cloud services change
- **CLI Friendly**: Easier navigation and scripting

### Limitations to Be Aware Of
- **Symlink Maintenance**: Need to update if underlying paths change
- **Application Compatibility**: Some apps may not fully support symlinks
- **Backup Considerations**: Need backup solutions that follow symlinks

### Maintenance Requirements
- **Periodic Verification**: Check symlinks are intact (quarterly)
- **Documentation**: Keep your logical-to-physical mapping updated
- **Graceful Upgrades**: When changing cloud services, update symlinks first

### Avoiding Pitfalls
- **Test on Small Scale**: Implement one section at a time
- **Backup Before Major Changes**: Always have Time Machine or other backups
- **Document Everything**: Keep notes on what links where


---



<!--### Some options for next steps:

1. Create the comprehensive Directory Structure document for your FOMO project
2. Develop detailed Hazel rules for Downloads+ management
3. Build more advanced CLI navigation scripts
4. Create a naming standards reference guide
5. Develop a migration strategy for existing files

Should I focus on any specific aspect of this implementation next? Perhaps detailed Hazel rules for the Downloads+ folder or automation scripts for maintaining this structure?-->




