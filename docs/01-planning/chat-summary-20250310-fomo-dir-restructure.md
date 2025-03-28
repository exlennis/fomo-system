# FOMO Directory Structure - Discussion Summary

Save these specific elements from our discussion would provide valuable context for creating the Directory Structure (fomo-directory-structure-v01.md) artifact:

1. **Mermaid Diagrams**: The storage architecture diagram and file processing flow charts provide visual context that would be valuable to include directly.

2. **Complete Directory Mapping**: The comprehensive physical/logical mapping we developed showing the "before" and "after" states is essential reference material.

3. **Assets vs Catalogues Concept**: Our philosophical discussion about the distinction between assets (the files themselves) and catalogues (the organizational systems) provides important conceptual framing.

4. **Symlink Directionality Explanation**: The technical reasoning for cloud → local symlinks would be valuable for implementation details.

5. **Multi-Machine Implementation Script**: The sample script showing how to adapt the setup for different machines provides practical implementation guidance.

These elements provide both the conceptual foundation and practical implementation details needed to create a comprehensive Directory Structure document. I would recommend starting a new chat with these specific components as reference material when we begin drafting the artifact.

---

## 1. Current System Analysis

### 1.1 Storage Locations
- **Home Directory** (`/Users/ez/`): Local files, applications, system
- **iCloud Drive**: Personal documents, Desktop sync, Downloads+
- **Dropbox**: Design projects, work documents, design assets
- **Local**: Development projects, app data, configuration files
- **Network Volumes**: Media files (current status pending verification)

### 1.2 Organization Patterns
- **Design Files**: Organised in Dropbox under `-DESIGN-`, `-PROJECTS-`, and `-WORK-`
- **Development**: Primarily in `/Local/-PROJECTS-Dev/`
- **Personal Documents**: In iCloud under `-PERSONAL-`, `-FAMILY-`, `-FINANCE-`
- **Downloads**: Split between local Downloads and iCloud `Downloads+`

### 1.3 Current Directory Depth
- Excessive nesting (often 5+ levels deep)
- Inconsistent naming approaches
- Mixed case conventions

## 2. Pain Points Identified

### 2.1 Primary Challenges
1. **Excessive Folder Depth**: Deep nesting in cloud storage making CLI navigation difficult
2. **Scattered Resources**: Assets, libraries, and templates dispersed across system
3. **Inconsistent Naming**: Lack of standardization in terminology and conventions

### 2.2 Secondary Issues
1. **Git & Knowledge Management**: Uncertainty about optimal Obsidian/Git integration
2. **Downloads Management**: Active area requiring automation and organization
3. **Multi-machine Synchronisation**: Need for consistent structure across devices


## 3. Proposed Directory Structure

### 3.1 Top-Level Architecture
```
~/ # Home directory 
├── Projects/ # Unified project access 
├── Resources/ # Centralized resources 
├── Knowledge/ # Knowledge management 
├── System/ # System configuration
├── Documents/ # Personal information 
│ └── Work/ # Work-related documents 
└── ... (standard macOS folders)
```

### 3.2 Physical to Logical Mapping
- **Cloud Storage Remains Intact**: Physical files kept in cloud locations
- **Symlinks Create Logical Structure**: Unified access through consistent paths
- **Directional Preference**: Cloud → Local symlinks establish cloud as "source of truth"

### 3.3 Renamed Cloud Folders
- **Dropbox**: `-DESIGN-` → `design`, `-PROJECTS-` → `projects`, `-WORK-` → `work`
- **Documents**: `-PERSONAL-` → `personal`, `-FAMILY-` → `family`, `-FINANCE-` → `finance`



## 4. File Processing Flow

### 4.1 Ingestion and Routing
- **Creation Sources**: Screenshots, downloads, design files, dev files
- **Initial Landing**: Downloads+ (iCloud) serves as centralized intake
- **Processing Pipeline**: inbox → processing → organized storage


### 4.2 Three-Stage Downloads Management
```
Downloads+/ 
├── inbox/ # Initial landing for files 
├── processing/ # Files being sorted/renamed 
└── archive/ # Temporary storage for processed files
```

## 5. Terminology Explorations

### 5.1 Organizational Concepts
- **Assets vs Catalogues**: Physical files vs organizational systems
  - Assets: The actual design/media elements themselves
  - Catalogues: Systems organizing and providing views into assets
- **Resources vs References**: Support materials vs informational content

### 5.2 Naming Standards Framework
- **Case Convention**: lowercase-kebab-case for directories and files
- **Prefix/Suffix Standards**:
  - State indicators as suffixes: `logo-working.ai`
  - Type indicators as prefixes: `tpl-invoice.docx`
  - Date stamps as prefixes: `20250310-meeting-notes.md`
  - Version numbers as suffixes: `proposal-v01.pdf`

## 6. Implementation Strategy

### 6.1 Setup Approach
- **Phased Implementation**: Start with high-value areas, gradually expand
- **Symlink Creation**: Script to establish logical structure
- **CLI Enhancement**: Shell aliases for improved navigation

### 6.2 Multi-Machine Considerations
- Use of `$HOME` variable for portability across machines
- Machine detection for device-specific configurations
- Consistent cloud → local symlink direction to maintain stability

## 7. Key Architecture Decisions

### 7.1 Structural Principles
- **Depth vs Breadth**: Preference for shallow hierarchy with clear grouping
- **Access Frequency**: Frequently used items closer to top level
- **Conceptual Grouping**: Items organized by purpose/function
- **Storage Independence**: Logical structure decoupled from physical storage

### 7.2 Symlink Philosophy
- **Direction**: Cloud → Local establishes cloud as authoritative source
- **Scope**: Higher-level symlinking preferred over granular links
- **Maintenance**: Structure designed for resilience during cloud service changes
