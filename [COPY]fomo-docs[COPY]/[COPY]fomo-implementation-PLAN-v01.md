# FOMO Implementation Plan v01

## 1. Introduction and Purpose

This implementation plan establishes a structured approach for deploying the File Organisation, Management & Optimisation (FOMO) system. It bridges theoretical frameworks and practical application, providing a clear roadmap for progressive adoption while minimising disruption to existing workflows.

### 1.1 Scope

This plan covers:
- Implementation of the FOMO directory structure
- Application of FOMO naming standards
- Integration of controlled vocabulary framework
- Deployment of automation tools and scripts
- Configuration of cross-platform consistency
- Training and habit formation approaches

### 1.2 Guiding Principles

The implementation process follows these core principles:

- **Progressive Adoption**: Forward-looking implementation takes priority over historical reorganisation
- **Value-Driven Prioritisation**: Focus on high-impact, low-effort changes first
- **Automation First**: Identify and implement automation opportunities early
- **Cross-Platform Consistency**: Maintain unified approach across applications and devices
- **Habit Formation**: Build sustainable usage patterns through consistent application
- **Adaptability**: Allow for refinement based on practical experience

### 1.3 Alignment with FOMO Documents

This implementation plan works in conjunction with:

- **fomo-project-charter-v03.md**: Overall vision and success criteria
- **fomo-naming-STANDARDS-v02.md**: File naming conventions
- **fomo-directory-structure-GUIDELINES-v03.md**: Folder organisation framework
- **fomo-controlled-VOCABULARY-v01.md**: Terminology standardisation
- **fomo-term-DICTIONARY-v01.md**: Term definitions and priority levels
- **fomo-flow-file-rename-process.svg**: Workflow diagram for file renaming
- **fomo-flow-file-type-detection-process.svg**: Workflow diagram for type detection
- **fomo-maintenance-log-v02.md**: System changes tracking

## 2. Technical Requirements and Dependencies

### 2.1 Required Tools

| Tool | Purpose | Status |
|------|---------|--------|
| Cloud storage services | Cross-device synchronisation | Required |
| Hazel | Automated file processing | Required |
| Apple Shortcuts | Workflow automation | Required |
| Python 3.10+ | Script execution | Required |
| Git | Version control | Required for development projects |
| n8n | Cloud workflow automation | Optional |
| Font management tool | Font library organisation | Recommended |


### 2.2 System Prerequisites

- **Operating System**: macOS Sonoma or later
- **Permissions**: Full disk access for automation tools
- **Cloud Services**: Properly configured Dropbox and iCloud accounts
- **Terminal Access**: Command-line capability for script execution
- **Backup System**: Time Machine or equivalent configured

### 2.3 Technical Considerations

- **Symlink Handling**: Follow precautions in directory structure guidelines section 7.3
- **Cloud Sync Conflicts**: Maintain proper directionality for all symlinks
- **Permissions Management**: Ensure automation tools have necessary file system access
- **Script Dependencies**: Verify Python packages and dependencies are installed

## 3. Phased Implementation Strategy

### 3.1 Phase 1: Foundation Setup (Week 1)

This phase establishes the core infrastructure and basic automations.

#### Objectives
- Create the base directory structure
- Establish essential symlinks
- Implement basic automation tools
- Configure cloud service integration
- Audit existing script repository

#### Entry Criteria
- All prerequisite tools installed
- Cloud services properly configured
- Backup system verified
- Documentation reviewed

#### Tasks

| Task | Description | Priority | Dependencies |
|------|-------------|----------|--------------|
| 1.1 | Audit existing script repository | High | None |
| 1.2 | Create base directory structure | Critical | None |
| 1.3 | Establish symlinks between cloud/local | Critical | Task 1.2 |
| 1.4 | Configure basic Hazel rules for Downloads | High | Tasks 1.2, 1.3 |
| 1.5 | Set up screenshot automation workflow | High | Tasks 1.2, 1.4 |
| 1.6 | Create file naming shortcuts | High | None |
| 1.7 | Implement controlled vocabulary framework | Medium | None |
| 1.8 | Create shell integration for quick navigation | Medium | Task 1.2 |
| 1.9 | Verify all symlinks function correctly | Critical | Task 1.3 |
| 1.10 | Create file type change shortcuts (kebab case, title case) | Medium | None |

#### Task Details

**Task 1.1: Audit Existing Script Repository**
- Categorise available scripts by function and applicability
- Evaluate compatibility with FOMO naming and structure conventions
- Identify scripts that can be immediately leveraged
- Prioritise scripts for modification or adaptation
- Document gaps where new scripts will need to be developed

**Task 1.2: Create Base Directory Structure**
```bash
# Create the core FOMO directories
mkdir -p ~/Projects/{dev,design,education}
mkdir -p ~/Resources/{assets,catalogues,inspirations,references,templates}
mkdir -p ~/Knowledge/{vault,docs}
mkdir -p ~/System/{configs,scripts,search}
mkdir -p ~/Downloads/{inbox,processing,archive}
```

**Task 1.3: Establish Symlinks**
Follow the procedure in directory structure guidelines section 7.3, ensuring existing directories are backed up before creating symlinks.

**Task 1.4: Configure Basic Hazel Rules**
Create rules for:
- Moving new downloads to inbox
- Processing common file types
- Archiving older files

**Task 1.5: Set Up Screenshot Automation**
- Configure screenshot location and naming
- Create Hazel rule for processing screenshots
- Implement screenshot file naming based on content/context

**Task 1.6: Create File Naming Shortcuts**
- Develop Apple Shortcuts for renaming selected files
- Add quick actions to context menus
- Create text replacement shortcuts for common patterns

**Task 1.7: Implement Controlled Vocabulary Framework**
- Focus on essential (•••) terms from the Term Dictionary
- Create reference sheets for common terms
- Develop tagging approach for key applications

**Task 1.8: Create Shell Integration**
Add to `.zshrc` or equivalent:
```bash
# Quick navigation to major areas
alias proj="cd ~/Projects"
alias res="cd ~/Resources"
alias know="cd ~/Knowledge"
alias sys="cd ~/System"
alias dl="cd ~/Downloads"

# Project jumping function
proj() {
    # Function implementation as specified in directory structure guidelines
}
```

#### Exit Criteria
- Directory structure established and verified
- Symlinks functioning correctly
- Basic automation tools operational
- Downloads workflow functioning
- File naming shortcuts available
- Script audit completed
- Shell integration verified
- Phase documented in maintenance log

#### Success Metrics
- 100% of symlinks established correctly
- Base directories match specification
- Screenshot automation workflow functioning
- At least 5 file naming shortcuts implemented
- Downloads processing automation operational

### 3.2 Phase 2: New Files Implementation (Week 2-3)

This phase focuses on forward-looking implementation for all new files.

#### Objectives
- Apply conventions to all new files
- Configure application save locations
- Implement file type detection automation
- Develop project templates

#### Entry Criteria
- Phase 1 completed successfully
- Foundation infrastructure verified
- Basic automation functioning

#### Tasks

| Task | Description | Priority | Dependencies |
|------|-------------|----------|--------------|
| 2.1 | Configure default save locations | High | None |
| 2.2 | Implement file naming shortcuts for common types | High | None |
| 2.3 | Set up type-specific automation rules | High | None |
| 2.4 | Create project templates with naming embedded | Medium | None |
| 2.5 | Configure email attachment handling | Medium | None |
| 2.6 | Implement browser download handling | High | None |
| 2.7 | Deploy cross-device synchronisation | Medium | None |
| 2.8 | Create tagging workflow for key applications | Medium | None |
| 2.9 | Develop font management workflow | Medium | None |
| 2.10 | Establish design asset organisation | High | None |

#### Task Details

**Task 2.1: Configure Default Save Locations**
For each primary application, set default save locations to align with FOMO structure:
- Design applications → ~/Projects/design/
- Development IDEs → ~/Projects/dev/
- Documents → ~/Documents/ (synced to iCloud)
- Templates → ~/Resources/templates/

**Task 2.2: Implement File Naming Shortcuts**
Create shortcuts for common file types based on the file rename process diagram:
- Document naming shortcuts
- Image file naming shortcuts
- Project file naming shortcuts
- Code file naming shortcuts

**Task 2.3: Set Up Type-Specific Automation Rules**
Implement Hazel rules based on the file type detection process diagram:
- Screenshot identification and processing
- Document processing
- Design file processing
- Default type handling

**Task 2.4: Create Project Templates**
Develop templates with embedded naming conventions for:
- Design projects
- Development projects
- Document collections
- Client projects

**Task 2.8: Create Tagging Workflow**
Following the Tag Management Guidelines:
- Implement tagging in Apple Notes
- Configure Gmail labels
- Set up Obsidian tags

#### Exit Criteria
- Default save locations configured
- File naming shortcuts functioning
- Type-specific automation rules operational
- Project templates available
- Cross-device synchronisation verified
- Tagging workflow established
- Font management system operational
- Phase documented in maintenance log

#### Success Metrics
- 90% of new files follow naming conventions
- Type detection accuracy > 95%
- Template usage for > 80% of new projects
- Cross-device consistency > 90%

### 3.3 Phase 3: Active Projects (Week 4-6)

This phase applies the FOMO system to current active projects.

#### Objectives
- Migrate active projects to FOMO structure
- Update existing references
- Refine automation based on usage

#### Entry Criteria
- Phases 1 and 2 completed successfully
- New file workflow functioning reliably
- Automation rules proven stable

#### Tasks

| Task | Description | Priority | Dependencies |
|------|-------------|----------|--------------|
| 3.1 | Inventory active projects | High | None |
| 3.2 | Prioritise projects for migration | High | Task 3.1 |
| 3.3 | Create migration plans for each project | Medium | Task 3.2 |
| 3.4 | Migrate development projects | Medium | Task 3.3 |
| 3.5 | Migrate design projects | Medium | Task 3.3 |
| 3.6 | Update application references | High | Tasks 3.4, 3.5 |
| 3.7 | Verify project functionality post-migration | Critical | Tasks 3.4, 3.5, 3.6 |
| 3.8 | Refine automation based on project needs | Medium | Task 3.7 |
| 3.9 | Update project documentation | Medium | Tasks 3.4, 3.5 |
| 3.10 | Develop project-specific naming guidance | Low | Tasks 3.4, 3.5 |

#### Task Details

**Task 3.1: Inventory Active Projects**
Create a comprehensive list of all active projects, including:
- Project name and type
- Current location
- Associated applications
- External dependencies
- Special considerations

**Task 3.2: Prioritise Projects for Migration**
Rank projects by:
- Activity level
- Complexity
- External dependencies
- Urgency
- Migration effort

**Task 3.3: Create Migration Plans**
For each project, document:
- Target directory structure
- File naming adjustments needed
- Application configuration changes
- Verification steps
- Rollback procedure

**Task 3.6: Update Application References**
For each application, update:
- Recent files lists
- Saved locations
- Project references
- Linked assets
- Configuration files

**Task 3.7: Verify Project Functionality**
After migration, verify:
- All files accessible
- Applications can find files
- External references intact
- Automation working correctly
- No unintended consequences

#### Exit Criteria
- Active projects migrated to FOMO structure
- Applications configured to use new locations
- Project functionality verified
- Documentation updated
- Phase documented in maintenance log

#### Success Metrics
- 100% of active projects migrated
- 0% functionality loss
- Application references updated
- Project documentation aligned with FOMO

### 3.4 Phase 4: Historical Content (Ongoing)

This phase gradually applies FOMO organisation to historical content as resources permit.

#### Objectives
- Identify high-value historical content
- Selectively migrate priority archives
- Document exceptions for legacy systems

#### Entry Criteria
- Phases 1-3 completed successfully
- Active projects functioning in new structure
- Automation proven reliable

#### Tasks

| Task | Description | Priority | Dependencies |
|------|-------------|----------|--------------|
| 4.1 | Inventory historical content | Medium | None |
| 4.2 | Categorise by value and access frequency | Medium | Task 4.1 |
| 4.3 | Create migration schedule | Low | Task 4.2 |
| 4.4 | Develop batch processing scripts | Medium | None |
| 4.5 | Migrate high-value historical content | Medium | Tasks 4.3, 4.4 |
| 4.6 | Document exceptions and special cases | Medium | Task 4.1 |
| 4.7 | Update search tools for legacy content | Low | None |
| 4.8 | Implement historical archiving policy | Low | None |
| 4.9 | Create retrieval guides for legacy systems | Low | Task 4.6 |
| 4.10 | Schedule periodic review sessions | Low | None |

#### Task Details

**Task 4.1: Inventory Historical Content**
Create inventory of:
- Archived projects
- Legacy client work
- Reference materials
- Design assets
- Documentation archives

**Task 4.2: Categorise by Value**
Rank historical content by:
- Reference frequency
- Future relevance
- Replacement difficulty
- Legal/contractual requirements
- Sentiment value

**Task 4.4: Develop Batch Processing Scripts**
Create scripts for:
- Batch file renaming
- Directory restructuring
- Metadata extraction
- Compliance checking
- Duplicate identification

**Task 4.6: Document Exceptions**
For content that won't be migrated, document:
- Current location
- Access methods
- Retention policy
- Special handling requirements
- Justification for exception

#### Exit Criteria
- High-value historical content migrated
- Exceptions documented
- Batch processing scripts operational
- Retrieval guides created
- Phase documented in maintenance log

#### Success Metrics
- 50% of high-value historical content migrated
- 100% of exceptions documented
- Successful retrieval of legacy content

## 4. Human Factors and Adoption

### 4.1 Habit Formation Strategy

Successful implementation requires developing new habits. The following strategies will support adoption:

- **Start Small**: Begin with simple, high-frequency actions
- **Visual Reminders**: Create desktop backgrounds with naming patterns
- **Contextual Triggers**: Link new habits to existing workflow steps
- **Consistent Application**: Apply conventions even when in a hurry
- **Regular Review**: Schedule weekly system check-ins
- **Celebrate Success**: Acknowledge improvements and progress

### 4.2 Training Approach

- **Reference Sheets**: Create quick-reference guides for common operations
- **Cheat Sheets**: Develop visual aids for naming patterns
- **Practical Exercises**: Practice with sample files
- **Progressive Complexity**: Master basics before advanced features
- **Just-in-time Learning**: Learn features as needed for specific tasks

### 4.3 Error Recovery

- **Mistake Identification**: Regularly check for non-compliant files
- **Correction Processes**: Establish clear steps for fixing errors
- **Learning Opportunities**: Use mistakes to refine system
- **Non-judgmental Approach**: Accept that adaptation takes time

## 5. Cross-Platform Consistency

### 5.1 Application-Specific Configurations

| Application | Configuration | Implementation Timing |
|-------------|---------------|------------------------|
| macOS Finder | Default locations, tags, saved searches | Phase 1 |
| Cloud Storage | Folder structure, selective sync | Phase 1 |
| Adobe Creative Cloud | File locations, asset management | Phase 2 |
| Development IDEs | Project locations, file templates | Phase 2 |
| Apple Notes | Folder structure, tagging system | Phase 2 |
| Email Clients | Label/folder alignment, attachment handling | Phase 2 |
| Obsidian | Vault structure, file naming, tags | Phase 2 |
| Browser | Download location, file handling | Phase 2 |

### 5.2 Cross-Device Implementation

- **Primary Mac**: Full implementation of all components
- **Secondary Devices**: Focused implementation based on use case
- **iOS Devices**: Cloud-based access with selective implementation
- **Shared Systems**: Limited implementation focusing on interoperability

### 5.3 Cloud Service Integration

- **iCloud**: Desktop, Documents, Downloads synchronisation
- **Dropbox**: Project files, assets, references, education materials
- **GitHub**: Development projects, automation scripts
- **Service-Specific Considerations**: Selective sync, ignored patterns

## 6. Backup and Recovery Strategy

### 6.1 Implementation Backups

Before significant changes:
- Create Time Machine backup
- Snapshot critical directories
- Document current state
- Verify cloud synchronisation
- Backup configuration files

### 6.2 Recovery Procedures

For each implementation task, document:
- Rollback steps
- Alternative approaches
- Restoration procedures
- Failure indicators
- External dependencies

### 6.3 Long-term Backup Strategy

- **Local Backups**: Time Machine for system-wide protection
- **Cloud Backups**: Service-specific for critical data
- **Version Control**: Git repositories for code and configuration
- **Configuration Backups**: System settings and application preferences
- **Verification**: Regular backup testing

## 7. Integration with Controlled Vocabulary

### 7.1 Implementation Approach

The controlled vocabulary will be implemented progressively, starting with the highest-priority terms:

- **Phase 1**: Essential (•••) terms from Term Dictionary
- **Phase 2**: Important (••) terms
- **Phase 3**: Specialised (•) terms
- **Phase 4**: Domain-specific extensions

### 7.2 Application Integration

| Application | Vocabulary Implementation | Phase |
|-------------|---------------------------|-------|
| Directory Structure | Level 1 and 2 terms | Phase 1 |
| File Naming | Core terminology | Phase 1 |
| Apple Notes | Tags aligned with vocabulary | Phase 2 |
| Email | Labels aligned with vocabulary | Phase 2 |
| Obsidian | Tags aligned with vocabulary | Phase 2 |
| Project Templates | Embedded terminology | Phase 2 |
| Automation Rules | Rule conditions based on terms | Phase 2 |

### 7.3 Vocabulary Evolution

As the controlled vocabulary framework evolves:
- Update automation rules
- Refine application configurations
- Align new terminology with existing patterns
- Document changes in Maintenance Log

## 8. Measurement and Evaluation

### 8.1 Implementation Metrics

| Metric | Baseline | Target | Measurement Method |
|--------|----------|--------|-------------------|
| File Location Time | 45-60 seconds | 50% reduction | Timed search tests |
| File Processing Time | 30 min/day | 75% reduction | Time tracking |
| Naming Compliance | 40% | 95% for new files | Monthly sampling |
| Organisation Consistency | 60% | 90% correct placement | Directory audits |
| Cognitive Load | 8-10 decisions | 80% reduction | User feedback |
| System Satisfaction | 5/10 | 8/10 rating | Self-assessment |
| Automation Coverage | 20% | 80% of routine tasks | Task inventory |
| Adoption Rate | 0% | 100% new, 50% historical | Compliance audits |

### 8.2 Evaluation Schedule

- **Weekly**: Quick check of recent files for compliance
- **Monthly**: System audit and metric collection
- **Quarterly**: Comprehensive review and refinement
- **Biannually**: Full system evaluation and planning

### 8.3 Continuous Improvement

- Document challenges in Maintenance Log
- Refine processes based on actual usage
- Adjust automation to address emerging patterns
- Update documentation to reflect practical experience

## 9. Maintenance Procedures

### 9.1 Regular Maintenance Tasks

| Task | Frequency | Description |
|------|-----------|-------------|
| Audit New Files | Weekly | Sample check of naming compliance |
| Clean Downloads | Weekly | Process lingering items in Downloads folders |
| Verify Symlinks | Fortnightly | Check all symlinks function correctly |
| Update Automation | Monthly | Refine rules based on usage patterns |
| Verify Backups | Monthly | Confirm backup systems are functioning |
| Vocabulary Updates | As needed | Incorporate terminology refinements |
| Script Updates | As needed | Modify scripts to address new requirements |
| Log Updates | As needed | Update Maintenance Log with system changes |

### 9.2 Maintenance Documentation

All maintenance activities should be recorded in the Maintenance Log, including:
- Changes to the system
- Issues encountered
- Solutions implemented
- Lessons learned
- Future improvements

### 9.3 Version Management

- Document version changes following FOMO version control procedures
- Create new document versions for significant changes
- Update references across documents when versions change
- Maintain consistent versioning across related documents

## 10. Connection to Other FOMO Documents

This Implementation Plan works in conjunction with other FOMO project documents to form a unified system:

- **fomo-project-charter.md**: Establishes the overall vision and principles
- **fomo-naming-standards.md**: Defines the file naming conventions
- **fomo-directory-structure.md**: Defines the folder hierarchy
- **fomo-controlled-vocabulary.md**: Standardised terms
- **fomo-term-dictionary.md**: Term definitions and priorities
- **fomo-tag-management-guidelines.md**: Tag usage across platforms
- **fomo-automation-overview.md**: Scripts and tools for file management
- **fomo-special-cases.md**: Exceptions to standard structure
- **fomo-maintenance-log.md**: Tracks changes and issues

## 11. Appendices

### Appendix A: Quick Reference Guides

- Naming patterns for common file types
- Directory structure reference
- Essential vocabulary terms
- Key automation shortcuts

### Appendix B: Script Templates

- File renaming script template
- Directory creation script template
- Compliance checking script template
- Batch processing script template

### Appendix C: Application-Specific Guides

- Adobe Creative Cloud configuration
- Development IDE setup
- Apple Notes organisation
- Email client configuration
- Obsidian vault structure

---

_Version History:_
- v01 - 2025-04-05: Initial implementation plan created
