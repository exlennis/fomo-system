# FOMO Directory Structure v01

## 1. Introduction and Purpose

### 1.1 Purpose

This document establishes the directory structure standards for the File Organisation, Management & Optimisation (FOMO) project. It provides a comprehensive framework for organising files and directories in a way that balances human usability with machine processing, while addressing the specific needs of design, development, and personal workflows.

### 1.2 Scope

These directory structure standards apply to:

- Personal computing environment across multiple machines
- Design projects and assets (including fonts, mockups, and client deliverables)
- Development projects and repositories
- Knowledge management resources
- System configuration and settings
- Cloud-synced and locally-stored files

### 1.3 Benefits

Implementing this directory structure will:

- Reduce folder depth and navigation complexity
- Centralise resources for easier discovery and access
- Create a consistent organisational approach across different machines
- Enable efficient command-line and GUI navigation
- Establish clear separation of concerns between different file types
- Support both cloud synchronisation and local optimisation
- Simplify backup and maintenance procedures
- Enhance automation capabilities for file management

### 1.4 Implementation Overview

This restructuring involves:

- **8 total symlinks** pointed from cloud storage to local directories
    - 2 existing symlinks (`iCloud/Desktop` and `iCloud/Documents`)
    - 2 additional iCloud symlinks to be created
    - 4 Dropbox symlinks to be created
- **4 new folders** at the home directory level (Projects, Resources, Knowledge, System)
- **4 backups** to be established, ensuring all information is either cloud-sourced or backed up

## 2. Core Principles

### 2.1 Logical Coherence

The directory structure should reflect conceptual relationships between files and their purposes, not merely their technical attributes.

### 2.2 Appropriate Depth

Limit directory nesting to 3-4 levels when possible to reduce navigation complexity and path length.

### 2.3 Separation of Concerns

Distinguish between different functional areas (projects, resources, knowledge, system) to clarify purpose and reduce cognitive load.

### 2.4 Physical vs Logical Distinction

Maintain a separation between physical storage locations (where files exist on disk or in cloud services) and logical organisation (how they appear to users and applications).

### 2.5 Cloud-Local Harmony

Ensure seamless integration between cloud-synced and locally-stored files while preserving appropriate separation.

### 2.6 Balancing Access vs Organisation

Organise by access frequency and relation rather than strict hierarchical taxonomies, placing frequently-accessed items closer to the top level.

### 2.7 Naming Convention Adherence

Apply consistent naming conventions throughout the filesystem structure:

- Always complete folder renaming in cloud locations *before* working on local folders.
- Use standardised naming formats according to level:
    - Top-level folders (level 1): One-word with capitalisation, following macOS convention (e.g., `Projects`, `Resources`).
    - Nested folders (level 2+): All lowercase preferred one-word (e.g., `archive`,`config`) use hyphens as separators when ncecssary (e.g., `archive-branding`, `env-path`).
    - Refer to `Controlled Vocabulary` 
- Make exceptions for top-level project and client folders, and domain-specific edge cases (e.g. font folders).

### 2.8 Backup Strategy

Ensure data protection through a comprehensive backup approach:

- Prioritise cloud storage for most active files
- Back up any locally-stored content not in cloud services
- Use Time Machine for system-wide protection
- Implement Git repositories for code and configuration files
- Maintain at least 4 backups to ensure all information is either cloud-sourced or backed up

## 3. Conceptual Framework

### 3.1 Assets vs Catalogues

A fundamental distinction in the FOMO system is between assets (the files themselves) and catalogues (the organisational systems):

- **Assets**: The actual files and content (images, documents, code, etc.)
- **Catalogues**: Systems that organise, index, and provide access to assets

This separation allows a single asset to be accessed through multiple organisational views without duplication. For example:

- A font file is an asset stored once physically
- It may appear in multiple catalogue systems (font manager, design project, system fonts)
- Changes to the asset propagate to all views automatically

### 3.2 Physical vs Logical Structure

The FOMO system distinguishes between:

- **Physical Structure**: Where files are actually stored on disk or in cloud services
- **Logical Structure**: How files are presented to users through the directory hierarchy

This separation is implemented through strategic use of symbolic links (symlinks), creating a consistent logical view regardless of the underlying physical storage.

### 3.3 Cloud Directionality

A critical principle for the FOMO system is the directionality of symlinks between cloud and local storage:

- Symlinks should always point FROM cloud storage TO local organisation
- This establishes cloud storage as the "source of truth"
- Changes in cloud services automatically reflect in the logical structure
- The approach minimises sync conflicts and circular reference issues

## 4. Glossary of Key Terms

This glossary defines important terminology used throughout the FOMO directory structure system:

### 4.1 Core Concepts

**Assets**: Actual files (primary content) like images, videos, audio, documents, and graphics that are stored, organised, and managed within the system.

**Metadata**: Information attached to assets that provides context, description, and helps in classification, searching and organising content.

**Catalogue (or Index)**: Organised and centralised listing of assets with detailed descriptions and metadata.

**Repository (or Collection)**: A centralised library where digital assets, often sharing common characteristics or purposes, are stored, organised, and systematically managed.

**Taxonomy**: A hierarchical classification system used to categorise and organise digital assets with similar characteristics.

### 4.2 Information Types

**References**: Supplemental materials or links that provide context, relationships, or additional information about the digital content. These are information consulted but rarely modified.

**Docs (Documentation)**: Written or digital materials that provide detailed guidance, instructions, and reference about a system, product, or process, facilitating understanding, implementation, and effective use.

**Guidelines**: Flexible recommended instructions or principles that provide guidance and direction, outline best practices, ensure consistency, and offer a framework for decision-making or action.

**Standards (or Specifications/Specs)**: Enforced requirements following a purposefully established ruleset to bring consistency, quality, and interoperability across systems and domains.

**Templates**: Predefined, reusable layouts or designs that can be used as a starting point for creating new content, ensuring consistency across different media items.

**Controlled Vocabulary**: A predefined list of standardised term used to sconsistently tag, categorise, and search digital assets. It ensures uniform metadata application, improves search accuracy, and helps efficiently organise and retrieve content across the system.

## 5. Top-Level Organisation 

### 5.1 Primary FOMO Directories

The FOMO directory structure establishes a clear, purpose-driven organisation at the top level of the user's home directory, while respecting macOS standard folders.

```
~/                           # Home directory
├── Projects/                # Work you're actively creating
├── Resources/               # Materials that support your work
├── Knowledge/               # Information you've collected or created
├── System/                  # Computer management and configuration
└── ... (standard macOS folders)
```

**Projects/**: Central location for active creation work
- Development projects (code repositories, applications)
- Design projects (client work, personal design projects)
- Current activities requiring significant ongoing effort

**Resources/**: Supportive materials used across projects
- Assets (design elements, media, templates)
- Reference materials (documentation, guides)
- Libraries (fonts, code libraries, design resources)

**Knowledge/**: Information collection and management
- Notes and personal knowledge base
- Documentation and reference materials
- Research and collected information

**System/**: Computer configuration and management
- Configuration files and settings
- Automation scripts and utilities
- System maintenance and monitoring tools

### 5.2 Standard macOS Integration

The FOMO structure integrates with standard macOS directories:

- Maintains standard `Desktop/`, `Documents/`, etc.
- Uses symlinks to integrate cloud-synced versions where appropriate
- Preserves system-expected locations for compatibility

## 6. Complete Directory Mapping

The complete logical directory structure provides a clean, purpose-driven organisation:

```
~/                                        # Home directory
├── Projects/                             # Container for active work (Level 1: Capitalized)
│    ├── dev/                             # Development projects (Level 2+: lowercase-kebab)
│    │    ├── project-one/                # Individual dev projects
│    │    └── project-two/
│    └── design/                          # Design projects
│         ├── client-a/                   # By client/category
│         └── client-b/
├── Resources/                            # Container for supportive materials
│    ├── assets/                          # Design/media elements
│    │    ├── fonts/                      # Typography resources
│    │    ├── icons/                      # Icon libraries
│    │    └── ... 
│    ├── catalogues/                      # Organisation systems for resources  
│    │    ├── font-manager-data/          # Metadata for font management
│    │    ├── asset-manager-data/         # Metadata for asset management
│    │    └── ...
│    ├── reference/                       # Information consulted but rarely modified
│    └── templates/                       # Starting points for new work
├── Knowledge/                            # Information management
│    ├── vault/                           # Personal knowledge management system
│    │    ├── notes/                      # Note collections
│    │    ├── journal/                    # Time-based entries
│    │    └── ...
│    └── docs/                            # Document library
├── System/                               # Computer management
│    ├── configs/                         # Application configurations
│    ├── scripts/                         # Automation scripts
│    └── search/                          # Saved searches and smart folders
├── Downloads/                            # Managed download location
│    ├── inbox/                           # New downloads landing area
│    ├── processing/                      # Files being sorted
│    └── archive/                         # Temporary storage for processed files
├── Desktop/                              # Standard macOS folder (synced to iCloud)
├── Documents/                            # Standard macOS folder (synced to iCloud)
│    ├── work/                            # Work-related documents
│    ├── personal/                        # Personal documents
│    ├── family/                          # Family-related documents
│    └── finance/                         # Financial documents
└── ... (other standard macOS folders)
```

> [!NOTE]
> Following FOMO naming conventions, Level 1 folders use macOS-style capitalisation (Projects, Resources, Knowledge, System), while nested folders use lowercase with hyphens as separators. Exceptions are made for top-level project and client folders, and domain-specific cases.

### 6.1 Physical to Logical Mapping

The physical storage locations are mapped to the logical structure through symlinks:

| Logical Path | Physical Location | 
|--------------|-------------------|
| ~/Projects/dev/ | → Local filesystem development projects |
| ~/Projects/design/ | → Dropbox/Projects |
| ~/Resources/assets/ | → Dropbox/Assets |
| ~/Resources/reference/ | → Dropbox/Docs |
| ~/Knowledge/vault/ | → iCloud Obsidian vault |
| ~/Knowledge/docs/ | → Dropbox/Docs |
| ~/Desktop/ | → iCloud synced Desktop |
| ~/Documents/ | → iCloud synced Documents |
| ~/Downloads/ | → iCloud Downloads+ |

### 6.2 Cloud Storage Organisation

The cloud storage remains organised according to its own structure, with the FOMO system creating a logical view:

**Dropbox:**
    ```
    Dropbox/
    ├── Assets/                               # Formerly -DESIGN-
    │    ├─── assets-library/                 # Eagle managed library
    │    ├─── fonts/                          # Organised font library
    │    ├─── colours/                        # Colour palette, swatch books
    │    └── ...
    ├── Docs/                                 # Documentation reference library
    ├── Projects/                             # Formerly -PROJECTS-
    └── ...
    ```

**iCloud Drive:**
    ```
    iCloud Drive/
    ├── Desktop/                              # Synced desktop (standard)
    ├── Documents/                            # Synced documents (standard)
    │    ├── personal/                        # Formerly -PERSONAL-
    │    ├── family/                          # Formerly -FAMILY-
    │    ├── finance/                         # Formerly -FINANCE-
    │    └── work/                            # Work documents (formerly in Dropbox)
    ├── Downloads/                            # Formerly Downloads+
    │    ├── inbox/
    │    ├── processing/
    │    └── archive/
    └── Obsidian/                             # Knowledge management vault
         └── ...
    ```

### 6.3 Media/Network-Attached Storage

Media content is structured on network storage for easy access and management:

```
Media/                                    # Network attached (renamed from ∆Media)
├── Books/                                # Calibre managed library
├── Movies/                               # Plex managed library
├── Music/                                # Plex managed library
├── Photos/                               # Plex managed library
├── Restricted/                           # Controlled access content
└── Shows/                                # Formerly TV Shows, Plex managed library
```

### 6.4 Symlink Strategy

1.  **Directionality Principle:** All symlinks follow a consistent direction:

    ```
    Cloud Storage Location --> Local Filesystem Location
    ```

    This approach:
    - Establishes cloud storage as the "source of truth"
    - Ensures changes in cloud services propagate to logical structure
    - Prevents circular references and sync conflicts
    - Maintains stability if local structure is reorganised

2.  **Implementation Guidelines:** When creating symlinks:

    - **Use Absolute Paths:** Always use complete paths from root for reliability.
    - **Point FROM Cloud TO Local:** Never link in the opposite direction.
    - **Higher-Level Linking:** Link entire directories rather than individual files when possible.
    - **Documentation:** Maintain a mapping of all symlinks for reference.
    - **Testing:** Verify sync functionality after creating each symlink.

3.  **Symlink Maintenance Considerations:** To ensure long-term stability:

    - **Periodic Verification:** Check symlinks quarterly for integrity.
    - **Change Management:** When changing cloud services, update symlinks before other changes.
    - **Backup Strategy:** Ensure backup systems properly handle symlinks.
    - **Sync Conflicts:** Handle by resolving in cloud location, then refreshing symlinks.

## 7. Implementation Instructions

### 7.1 Preparation

Before implementing the structure:

1.  **Backup System**: Create a complete Time Machine or equivalent backup
2.  **Cloud Sync**: Ensure all cloud services are fully synced
3.  **Rename Cloud Folders**: Standardise name formats in cloud locations first, following the naming conventions:
    - Level 1 folders: One-word with capitalisation (e.g., Assets, Docs, Projects)
    - Nested folders: lowercase with hyphens (e.g., client-projects, design-templates)
4.  **Document Existing Structure**: Map your current setup for reference

### 7.2 Core Structure Creation

Create the base directory structure:

    ```bash
    # Create the core FOMO directories
    mkdir -p ~/Projects/{dev,design}
    mkdir -p ~/Resources/{assets,catalogues,reference,templates}
    mkdir -p ~/Knowledge/{vault,docs}
    mkdir -p ~/System/{configs,scripts,search}
    mkdir -p ~/Downloads/{inbox,processing,archive}
    ```

### 7.3 Symlink Establishment

Set up the symlinks from cloud to local directories:

    ```bash
    # Dropbox symlinks
    ln -sf "$HOME/Library/CloudStorage/Dropbox-Personal/Assets" "$HOME/Resources/assets"
    ln -sf "$HOME/Library/CloudStorage/Dropbox-Personal/Docs" "$HOME/Resources/reference"
    ln -sf "$HOME/Library/CloudStorage/Dropbox-Personal/Projects" "$HOME/Projects/design"
    ln -sf "$HOME/Library/CloudStorage/Dropbox-Personal/Docs" "$HOME/Knowledge/docs"
    
    # iCloud symlinks
    ln -sf "$HOME/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes" "$HOME/Knowledge/vault"
    ln -sf "$HOME/Library/Mobile Documents/com~apple~CloudDocs/Downloads/inbox" "$HOME/Downloads/inbox"
    ln -sf "$HOME/Library/Mobile Documents/com~apple~CloudDocs/Downloads/processing" "$HOME/Downloads/processing"
    ln -sf "$HOME/Library/Mobile Documents/com~apple~CloudDocs/Downloads/archive" "$HOME/Downloads/archive"
    ```

> [!NOTE]
> Both `~/Resources/reference/` and `~/Knowledge/docs/` intentionally point to the same `Dropbox/Docs` location, providing two different logical access points to the same content. This design allows the content to be accessed in different contexts—as reference material within Resources or as documentation within Knowledge.

### 7.4 Shell Integration

Add quick navigation functions to your `.zshrc` or equivalent:

    ```bash
    # Add to your .zshrc
    # Quick navigation to major areas
    alias proj="cd ~/Projects"
    alias res="cd ~/Resources"
    alias know="cd ~/Knowledge"
    alias sys="cd ~/System"
    alias dl="cd ~/Downloads"
    
    # Project jumping function
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

### 7.5 Phased Implementation

Implement the structure in phases:

1.  **Phase 1 (Days 1-2)**: Set up core structure and initial symlinks
2.  **Phase 2 (Days 3-7)**: Migrate active projects and high-value resources
3.  **Phase 3 (Days 8-14)**: Establish downloads workflow and automation
4.  **Phase 4 (Ongoing)**: Gradually reorganise historical content as needed

## 8. Migration Strategy

### 8.1 Pre-Migration Assessment

Before beginning migration:
1.  **Inventory Existing Files**: Document your current directory structure
    - Use tools like `find` or `ls -R` to capture the current state
    - Note existing naming patterns and conventions
    - Identify problematic areas with excessive nesting or inconsistent organization

2.  **Identify Content Categories**: Group content by type
    - Active projects vs. archived work
    - Shared resources vs. project-specific assets
    - System configurations and settings
    - Knowledge and reference materials

3.  **Flag High-Priority Items**: Mark actively used files and directories
    - Current client projects
    - Frequently accessed resources
    - Critical system configurations
    - Regular workflow files

4.  **Document Application Settings**: Note paths in applications that may need updating
    - Design application libraries and preferences
    - Development environment configurations
    - Browser download locations
    - Backup software settings

### 8.2 Phased Migration Approach

Implement migration in these four phases:

#### Phase 1: Core Structure 

- Create the FOMO directory structure
- Establish symlinks
- Test with small sample files
- Do not migrate actual content yet

#### Phase 2: Active Projects 

- Begin with 1-2 active projects
- Move to appropriate locations in ~/Projects/
- Update application references
- Test workflows before continuing

#### Phase 3: Resources & Knowledge 

- Reorganize design assets into ~/Resources/assets/
- Set up knowledge management in ~/Knowledge/
- Migrate templates and reference materials
- Configure cataloguing systems

#### Phase 4: Historical Content (Ongoing)

-   Gradually migrate archived projects.
-   Apply naming conventions to historical files.
-   Document exceptions for legacy materials.

### 8.3 Project-Specific Migration Guidelines

#### Design Projects

1.  Create project folder in `~/Projects/design/[client-name]/`.
2.  Move design source files, maintaining version history.
3.  Extract shared assets to `~/Resources/assets/`.
4.  Update application libraries to new locations.

#### Development Projects

1.  Clone repositories to `~/Projects/dev/`.
2.  Update local references and configuration.
3.  Add shared code libraries to appropriate locations.
4.  Configure IDEs to use new paths.

#### Knowledge and Documents

1.  Move reference materials to `~/Knowledge/docs/`.
2.  Import notes into a knowledge management system.
3.  Establish links between related content.
4.  Set up automated organization where possible.

### 8.4 Post-Migration Verification

After migrating each section:

1.  **Verify Access:** Ensure all files can be accessed through the new structure.
2.  **Test Applications:** Confirm that applications can find relocated files.
3.  **Check Symlinks:** Validate that all symlinks are working correctly.
4.  **Document Changes:** Update project documentation with new locations.

## 9. Multi-Machine Implementation

### 9.1 Setup Script

Use this script to establish consistent structure across machines:

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
    ICLOUD_PATH="$HOME/Library/Mobile Documents/com~apple~CloudDocs"
    OBSIDIAN_PATH="$HOME/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes"
    
    # Create base directories
    mkdir -p "$HOME/Projects"/{dev,design}
    mkdir -p "$HOME/Resources"/{assets,catalogues,reference,templates}
    mkdir -p "$HOME/Knowledge"/{vault,docs}
    mkdir -p "$HOME/System"/{configs,scripts,search}
    mkdir -p "$HOME/Downloads"/{inbox,processing,archive}
    
    # Set up symlinks based on machine type
    echo "Setting up for $MACHINE_TYPE machine..."
    
    # Common symlinks across all machines
    ln -sf "$DROPBOX_PATH/Assets" "$HOME/Resources/assets"
    ln -sf "$OBSIDIAN_PATH" "$HOME/Knowledge/vault"
    ln -sf "$DROPBOX_PATH/Docs" "$HOME/Resources/reference"
    ln -sf "$DROPBOX_PATH/Projects" "$HOME/Projects/design"
    ln -sf "$DROPBOX_PATH/Docs" "$HOME/Knowledge/docs"
    ln -sf "$ICLOUD_PATH/Downloads/inbox" "$HOME/Downloads/inbox"
    ln -sf "$ICLOUD_PATH/Downloads/processing" "$HOME/Downloads/processing"
    ln -sf "$ICLOUD_PATH/Downloads/archive" "$HOME/Downloads/archive"
    
    # Machine-specific configurations
    if [ "$MACHINE_TYPE" = "server" ]; then
    # Server-specific settings
    echo "Adding server-specific configurations..."
    # Additional server-specific symlinks
    elif [ "$MACHINE_TYPE" = "work" ]; then
    # Work machine settings
    echo "Adding work machine configurations..."
    # Work-specific configurations
    else
    # Personal machine gets everything
    echo "Adding personal machine configurations..."
    # Full personal setup
    fi
    
    echo "Directory structure created successfully for $MACHINE_TYPE!"
    ```

### 9.2 Machine-Specific Considerations

Adapt the structure for different environments:

**Personal Machine**:
- Full implementation of all directories
- Complete set of symlinks
- Media access paths to home server

**Work Machine**:
- Limited personal content
- Expanded work-related directories
- Stricter separation between work and personal

**Server/Home Machine**:
- Enhanced media directories
- Backup configurations
- Reduced development environment

### 9.3 Consistency Guidelines

To maintain consistency across machines:

1. **Use Relative Paths**: When possible, use $HOME instead of hardcoded paths
2. **Machine Detection**: Use hostname or other identifiers to apply appropriate settings
3. **Configuration Files**: Store machine-specific configurations in version control
4. **Synced Settings**: Keep shell aliases and functions consistent via dotfiles repository

## 10. Special Considerations

### 10.1 Downloads Management

The three-stage Downloads structure provides a clear workflow:

1. **inbox/**: All new files land here initially
   - Set as default download location in browsers
   - Configure screenshots to save here
   - First target for automation rules

2. **processing/**: Files actively being sorted
   - Temporary staging area
   - Files moved here during processing
   - Hazel monitors for automated sorting

3. **archive/**: Temporary storage for processed files
   - 30-day holding area before deletion
   - Last chance to recover accidentally processed files
   - Automatic cleanup after retention period

### 10.2 Font Management

Fonts require special handling due to their dual nature:

1. **Storage Location**: `~/Resources/assets/fonts/`
   - Organised by family/style following typography standards
   - Retains PascalCase naming per FOMO Naming Standards

2. **Font Management Tool Integration**:
   - Font manager data stored in `~/Resources/catalogues/font-manager-data/`
   - Activation states managed through font management software
   - Variable fonts handled according to industry standards

### 10.3 Git Repository Organisation

Git repositories have specific requirements:

1. **Development Projects**: `~/Projects/dev/[project-name]/`
   - Each repository in its own directory
   - Follow language/framework conventions within repos
   - Example: `~/Projects/dev/fomo-system/`

2. **Knowledge Management**: Git repositories within Obsidian vault
   - Selective tracking of text content
   - `.gitignore` configured to exclude binary files
   - Example: `~/Knowledge/vault/notes/.git/`

3. **System Configuration**: Version-controlled dotfiles
   - Stored in `~/System/configs/dotfiles/`
   - Includes shell configurations, application settings
   - Symlinked to appropriate locations

### 10.4 Cloud Service Considerations

Each cloud service has unique characteristics to consider:

**Dropbox**:
- Optimised for shared project files
- Handles large binary files well
- Reliable symlink handling
- Used for design assets and projects

**iCloud**:
- Deep macOS integration
- Variable offline file handling
- Desktop and Documents syncing enabled
- Better for frequently changed text files

**Local Storage**:
- Used for development files requiring fast access
- Appropriate for large multimedia projects
- Houses git repositories with frequent operations
- Requires separate backup strategy

## 11. Maintenance Procedures

### 11.1 Regular Verification

Perform these checks to ensure system integrity:

1.  **Weekly Quick Check**:
    - Verify core symlinks are functioning
    - Check Downloads workflow is processing correctly
    - Confirm new files are appearing in correct locations

2.  **Monthly System Review**:
    - Validate all symlinks in the structure
    - Check cloud service sync status
    - Review folder growth and storage usage
    - Identify potential reorganisation opportunities

3.  **Quarterly Deep Audit**:
    - Run directory structure validation scripts
    - Update machine-specific configurations
    - Review and update automation rules
    - Check compliance with naming conventions

### 11.2 Backup Management

Ensure comprehensive data protection:

1.  **Cloud-Synced Content**:
    - Verify cloud services are syncing correctly
    - Confirm all symlinks are properly connected to cloud sources
    - Test cloud service recovery functionality periodically

2.  **Local-Only Content**:
    - Identify any content not stored in cloud services
    - Ensure Time Machine backups are current for system-wide protection
    - Use Git repositories for code, configuration files, and documentation
    - Consider additional backup solutions for critical local-only data

3.  **Backup Verification**:
    - Regularly test recovery from backups
    - Document backup locations and procedures
    - Maintain at least 4 backups to ensure all information is either cloud-sourced or backed up
    - Verify backup integrity quarterly

### 11.3 Troubleshooting Common Issues

Guidelines for resolving typical problems:

1.  **Broken Symlinks**:
    - Check if target exists in cloud storage
    - Verify cloud service is properly synced
    - Recreate symlink with correct target
    - Example: `ln -sf "[correct-cloud-path]" "[local-path]"`

2.  **Cloud Sync Conflicts**:
    - Resolve at the cloud storage level first
    - Never create bidirectional symlinks
    - After resolution, refresh affected symlinks
    - Consider temporarily disconnecting problem symlinks

3.  **Path Too Long Errors**:
    - Identify problematic deep paths
    - Restructure to reduce directory depth
    - Create higher-level symlinks where appropriate
    - Consider shorter directory names in deep structures

### 11.4 Adapting the Structure

Guidelines for evolving the system over time:

1.  **Adding New Directories:**
    - Follow existing naming patterns.
    - Place at the appropriate level in the hierarchy.
    - Update documentation to reflect changes.
    - Example: Adding `~/Resources/courses/` for educational materials.

2.  **Retiring Directories:**
    - Archive content if potentially needed.
    - Remove symlinks before deleting targets.
    - Update shell aliases and scripts.
    - Document changes in the maintenance log.

3.  **Cloud Service Changes:**
    - Document the existing symlink structure before making changes.
    - Update cloud paths at the source first.
    - Recreate symlinks after cloud reorganization.
    - Test thoroughly after migration.

## 12. Examples and Use Cases

### 12.1 Design Workflow Example

```
  # Starting a new client project
  mkdir -p ~/Projects/design/acme-corp/website
  mkdir -p ~/Projects/design/acme-corp/website/{briefs,design,assets,production}
  
  # Creating design assets
  touch ~/Projects/design/acme-corp/website/assets/acme-logo-primary-v01.ai
  touch ~/Projects/design/acme-corp/website/assets/acme-header-homepage-v01.psd
  
  # Design handoff for development
  mkdir -p ~/Projects/design/acme-corp/website/production
  touch ~/Projects/design/acme-corp/website/production/acme-website-homepage-handoff-v01.sketch
```

### 12.2 Development Workflow Example

```
  # Starting a new development project
  cd ~/Projects/dev
  git clone https://github.com/username/project-name.git
  cd project-name
  
  # Setting up project structure
  mkdir -p src/{components,utils,styles}
  mkdir -p docs
  touch README.md
  
  # Working on features
  touch src/components/Button.tsx
  touch src/utils/api-client.js
```

### 12.3 Knowledge Management Example

```
  # Creating new notes
  cd ~/Knowledge/vault/notes
  touch project-research-fomo.md
  mkdir -p reference/design-systems
  touch reference/design-systems/atomic-design-principles.md
  
  # Organising documentation
  cd ~/Knowledge/docs
  mkdir -p tutorials/css
  touch tutorials/css/grid-layout-guide.md
```

### 12.4 Downloads Processing Example

```
  # Browser downloads file to inbox
  # ~/Downloads/inbox/random-download.pdf
  
  # Hazel moves to processing for renaming
  # ~/Downloads/processing/random-download.pdf → client-presentation-20250301.pdf
  
  # File is moved to final destination
  # ~/Projects/design/client/presentations/client-presentation-20250301.pdf
  
  # If file isn't moved within 30 days, it goes to archive
  # ~/Downloads/archive/client-presentation-20250301.pdf
  
  # After 30 days in archive, it's automatically deleted
```

## 13. Integration with other FOMO Documents

This Directory Structure document works in conjunction with other FOMO project documents:

- **Naming-Standards-v02.md**: Defines the file naming conventions used within this structure
- **Project-Charter-v01.md**: Establishes the overall vision and principles for the FOMO system
- **Implementation-Plan-v01.md**: Details the step-by-step approach for system deployment
- **Maintenance-Log-v01.md**: Tracks changes and issues encountered during implementation
- **Special-Cases-v01.md**: Provides guidance for exceptions to the standard structure

## 14. Success Measures

The effectiveness of this directory structure will be measured by:

- **Navigation Efficiency**: 50% reduction in path depth and navigation time
- **Resource Location**: 70% faster retrieval of commonly used files
- **Cross-Machine Consistency**: 95% structural similarity across different devices
- **Automation Success**: 80% of file organisation handled automatically
- **Cognitive Load**: 60% reduction in decision points during file operations
- **Shell Navigation**: 40% reduction in CLI keystrokes for common operations
- **Multi-System Harmony**: Zero sync conflicts due to symlink issues

---

_Version History:_

- v01 - 2025-03-10: Initial directory structure document created


<!--
## Review
Below is a critical review of the "FOMO Directory Structure v01" document, evaluating its strengths, identifying potential areas for improvement, and ensuring alignment with its stated principles. This analysis aims to provide a comprehensive assessment to help refine and optimize the proposed file organization system. 

Refinements to enhance its effectiveness:

- Clarify the symlink count and list all 8 explicitly.
- Integrate Downloads workflow details (tools, retention) into core sections.
- Specify backup coverage for local content like font manager data and Git repositories.
- Address offline access to mitigate cloud dependency risks.
- Provide or reference validation scripts and enhance the `proj` function.

With these adjustments, the document will offer an even more robust and user-friendly system, fully realizing its goals of reducing navigation complexity, centralizing resources, and ensuring consistency across machines.

### 1. Symlink Count Discrepancy
- **Issue**: The implementation overview claims "8 total symlinks," but the document explicitly lists only 7 in the symlink establishment section:
  - **Dropbox (4)**: `Assets` → `~/Resources/assets`, `Docs` → `~/Resources/reference`, `Projects` → `~/Projects/design`, `Docs` → `~/Knowledge/docs`
  - **iCloud (3)**: `Obsidian` → `~/Knowledge/vault`, `Downloads/inbox` → `~/Downloads/inbox`, `Downloads/processing` → `~/Downloads/processing`, `Downloads/archive` → `~/Downloads/archive`
- **Analysis**: The "2 existing symlinks" (`iCloud/Desktop` and `iCloud/Documents`) are likely included in the total of 8, but this isn’t explicitly clarified in the symlink establishment section. The text mentions "2 additional iCloud symlinks," which may imply `Downloads` and `Obsidian`, but the three `Downloads` subfolders complicate the count.
- **Recommendation**: Explicitly list all 8 symlinks in Section 7.3 (Symlink Establishment) or clarify that the existing `Desktop` and `Documents` symlinks are part of the total, adjusting the "additional" terminology accordingly.

### 2. Downloads Workflow Details
- **Issue**: The three-stage Downloads structure (`inbox`, `processing`, `archive`) is well-designed, but lacks specifics on automation tools and retention policies in the main text.
- **Analysis**: Section 10.1 mentions Hazel for `processing` and a 30-day retention for `archive`, but these details are not integrated into the core structure description (Section 5) or implementation instructions (Section 7).
- **Recommendation**: Briefly note the intended automation tool (e.g., "Hazel or similar") in Section 5.1 and specify the retention period (e.g., "30 days before automatic deletion") in Section 5 or 7 to ensure clarity for implementers.

### 3. Font Management Ambiguity
- **Issue**: Fonts are stored in `~/Resources/assets/fonts/` (symlinked to `Dropbox/Assets`), but the location of font manager data (`~/Resources/catalogues/font-manager-data/`) is not specified as cloud-synced or local.
- **Analysis**: If local, this data isn’t covered by the cloud backup strategy, which could risk data loss. The separation aligns with the assets vs. catalogues principle, but its physical storage needs clarification.
- **Recommendation**: Specify whether `font-manager-data` is local or cloud-synced, and if local, include it explicitly in the backup strategy (e.g., via Time Machine).

### 4. Git Repository Backup
- **Issue**: Git repositories in `~/Projects/dev/` are local for performance, but the document doesn’t detail their backup beyond mentioning Git usage.
- **Analysis**: Local repositories risk data loss without a clear backup plan, especially since they aren’t cloud-synced by default. The **backup strategy** principle requires comprehensive coverage.
- **Recommendation**: Add a note in Section 2.9 or 10.3 specifying backup options for Git repositories (e.g., regular pushes to remote hosting services like GitHub or inclusion in Time Machine backups).

### 5. Offline Access Considerations
- **Issue**: The heavy reliance on cloud storage via symlinks doesn’t address scenarios where cloud access is unavailable (e.g., offline work).
- **Analysis**: This could disrupt workflows, especially for design or development tasks requiring constant file access. The **cloud-local harmony** principle could be extended to cover such cases.
- **Recommendation**: Include a brief section or note in Section 6 (Symlink Strategy) or 10 (Special Considerations) suggesting strategies like selective local caching or offline copies for critical files.

### 6. Validation Script Reference
- **Issue**: Section 11.1 mentions "directory structure validation scripts" for quarterly audits but doesn’t provide or reference them.
- **Analysis**: This omission reduces the document’s self-contained utility, as users must create these scripts independently.
- **Recommendation**: Include a simple example script (e.g., to check symlink integrity) in an appendix or reference an external resource in Section 11.

### 7. Shell Integration Enhancement
- **Issue**: The `proj` function in Section 7.4 navigates to the first matching project directory but doesn’t handle multiple matches.
- **Analysis**: If multiple projects match (e.g., `proj client` for `client-a` and `client-b`), users may need to refine their search manually, reducing efficiency.
- **Recommendation**: Enhance `proj` to list all matches if multiple exist (e.g., using a `select` menu or echo list), improving usability.

-->