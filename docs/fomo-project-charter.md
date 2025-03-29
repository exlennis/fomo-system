# FOMO Project Charter

## 1. Overview and Vision

The File Organisation, Management & Optimisation (FOMO) project aims to create a practical file management system with clear naming conventions and directory structures. This system will balance human readability with machine processing requirements, enabling consistent application and automation across personal and professional contexts.

> Why the name FOMO? Because there's a "fear of missing out" on one special character that could cause mayhem for both humans and agents.

The project envisions an elegant framework that is:

- Clear and concise for ease of implementation
- Structured but not limiting
- Adaptable to diverse file types and workflows
- Optimised for both human understanding and machine processing
- Implemented progressively to minimise disruption

## 2. Scope and Stakeholders

### Project Scope

#### In Scope

- **Design Projects**: Phase and revision-based files with visual references and long-term deliverables
- **Development Projects**: Language-specific naming requirements optimised for CI/CD practices
- **Personal Files**: Screenshots, invoices, documents, and work files requiring varied organisation
- **Special Collections**: Font libraries, design assets, Markdown notes, and reference materials
- **Automation Scripts**: Creation of tools for file management and organisation
- **Automation Scripts**: Creation of tools for file management and organisation, including file renaming, directory structure visualisation, and compliance reporting
- **Documentation**: Comprehensive guides, standards, and reference materials

#### Out of Scope

- **Enterprise-wide deployment**: Solutions focus on personal and small team usage
- **Third-party system integration**: Beyond essential cloud storage services
- **Historical reorganisation**: Complete reorganisation of all legacy content
- **Custom application development**: Beyond basic scripts and automation rules

### Key Stakeholders

- **Primary User**: The designer/developer implementing and maintaining the system
- **Automation Agents**: Terminal-based tools and scripts managing routine operations
- **Collaborators**: Other systems and users interacting with the organised files
- **Potential Future Users**: Team members who may adopt the system
- **Service Integrations**: Cloud storage, version control, and design tools interacting with the file system

## 3. Guiding Principles

1. **Clarity Over Complexity**: Prioritise understandable structures over intricate systems
2. **Balanced Standards**: Find the middle ground between rigorous rules and practical application
3. **Pattern-Based Design**: Incorporate actual usage patterns into system design
4. **Dual Readability**: Ensure compatibility with both human cognition and machine processing
5. **Phased Implementation**: Roll out changes gradually to reduce disruption and allow adaptation

## 4. Approach and Methodology

The FOMO project adopts a systematic yet flexible approach:

- **Research-Driven Design**: Base decisions on thorough investigation of best practices
- **Progressive Implementation**: Start with new files and work backwards to historical content
- **Automation-First Mindset**: Prioritise automated solutions using Hazel, Shortcuts, Python, and n8n
- **Human-Agent Collaboration**: Leverage Claude's capabilities alongside human expertise
- **Continuous Refinement**: Regularly evaluate and improve the system based on real-world usage
- **Claude Integration**: Harness Claude's project management, documentation, and analytics capabilities
- **GitHub Repository**: Maintain version-controlled documentation and scripts in a structured repository for accessibility and collaboration

## 5. Project Structure

The FOMO project is organised within Claude with interconnected conversations and artefacts. The Core Conversations and related artefacts are:

### Core Conversations

1. **Main System Planning**: Central hub coordinating all aspects and housing final documents
    - _Project Charter_ — This document, providing strategic overview
    - _Project Checklist_ — Task tracking and progress monitoring
2. **Research and Standards**: Focuses on naming conventions, directory structures, and best practices
    - _Naming Standards_ — Full naming convention guide
    - _Directory Structure_ — Folder hierarchy and organisation standards
3. **Workflow and Process Analysis**: Maps file creation paths and identifies automation opportunities
    - Develop process flow diagrams using Mermaid
    - Use analytics tool to analyse sample file datasets
    - Use analytics tool to identify patterns in current workflows
    - Create workflow diagrams for documentation
    - Map file creation sources and destinations
    - Identify manual tasks for potential automation
4. **Implementation and Automation**: Develops scripts, Hazel rules, and technical solutions
    - _Implementation Plan_ — Phased approach for system deployment
    - _Automation Scripts Overview_ — Summary of Technical solutions for file management
    - Create individual code artefacts
5. **Special Cases and Exceptions**: Addresses edge cases and unique file handling requirements
    - _Special Cases_ — Guidelines for exceptions and edge cases
    - _Naming Cheatsheet_ — Quick reference for daily application
    - _Maintenance Log_ — Historical record of system changes

## 6. Key Deliverables

### Documentation (Artefacts)

1. Overview of project (fomo-project-charter-v##.md)
2. Project management tracking (fomo-project-checklist-v##.md)
3. Detailed naming standards (fomo-naming-standards-v##.md)
4. Directory structure guidelines (fomo-directory-structure-v##.md)
5. Mermaid process flow diagram (fomo-process-diagram-v##.mmd)
6. Implementation plans (fomo-implementation-plan-v##.md)
7. Automation scripts documentation (fomo-automation-overview-v##.md)
8. Edge cases handling procedures (fomo-special-cases-v##.md)
9. Quick-reference cheatsheets (fomo-cheatsheet-v##.md)
10. Maintenance logs (fomo-maintenance-log-v##.md)

### Technical Solutions

1. Hazel Configuration
    - Create rule sets for different folders
    - Define pattern matching for file types
    - Establish naming transformations, apply naming conventions to screenshots
    - Set up sorting rules, Move files to appropriate directories based on type
2. Apple Shortcuts
    - Quick renaming of selected files
    - Capture and process screenshots
    - Standardise naming on save dialogs
    - Build file processing workflows
3. Scripts (Python, AppleScript and other)
    - Batch rename based on conventions
    - Analyse compliance with standards
    - Generate reports on system organisation
    - Directory structure visualisation tools
    - File system analysis scripts
4. n8n Workflows
    - Automate file processing for cloud services
    - Monitor and organise shared files
    - Integrate with other services

### Implementations

- Standardised directory hierarchy
- Automated file naming and processing
- Integrated workflow procedures
- Regular maintenance routines
- Centralised script repository at ~/System/scripts/
- Documentation repository at ~/Knowledge/docs/

## 7. Success Criteria

The FOMO project will be evaluated based on:

| Criterion                | Current Baseline | Target                   | Current Status     | Measurement        | Priority |
| ------------------------ | ---------------- | ------------------------ | ------------------ | ------------------ | -------- |
| File Location Speed      | 45-60 seconds    | 50% reduction            | 60% reduction      | Timed search tests | High     |
| Processing Time          | 30 min/day       | 75% reduction            | 65% reduction      | Time tracking      | High     |
| Naming Compliance        | 40%              | 95% for new files        | 90% for new files  | Monthly sampling   | Medium   |
| Organisation Consistency | 60%              | 90% correct placement    | 85% placement      | Directory audits   | Medium   |
| Cognitive Load           | 8-10 decisions   | 80% reduction            | 70% reduction      | User feedback      | High     |
| System Satisfaction      | 5/10             | 8/10 rating              | 7/10 rating        | Self-assessment    | Medium   |
| Automation Coverage      | 20%              | 80% of routine tasks     | 70% of tasks       | Task inventory     | High     |
| Adoption Rate            | 0%               | 100% new, 50% historical | 95% new, 30% hist. | Compliance audits  | Low      |

## 8. Implementation Timeline

The project will be implemented in four phases:

1. **Foundation Setup** (1 week)
    - Finalise core documentation
    - Establish test environment
    - Create initial automation scripts
2. **New Files Implementation** (2 weeks)
    - Apply conventions to all new files
    - Configure Hazel rules and Shortcuts
    - Test automation in controlled settings
3. **Active Projects** (2 weeks)
    - Implement standards on current projects
    - Update document references
    - Refine automation based on usage
4. **Historical Content** (Ongoing)
    - Gradually apply standards to archived content
    - Prioritise high-value historical files
    - Document exceptions as needed

## 9. Key Technical Decisions

Based on initial research, these foundational decisions will guide implementation:

- **File Naming Convention**: kebab-case (hyphen-delimited)
    - Example: `project-name-document-v01.pdf`
    - Rationale: Optimal balance of readability, URL compatibility, and automation support
- **Date Format**: ISO 8601 (YYYYMMDD)
    - Example: `project-meeting-notes-20250301.md`
    - Rationale: Ensures chronological sorting and international compatibility
- **Version Numbering**: v01, v02 format with leading zeros
    - Example: `presentation-client-v03.pptx`
    - Rationale: Maintains correct sorting order in file listings
- **Special Character Policy**: Minimal use for maximum compatibility
    - Prohibited: `!@#$%^&*()=+[]{};:'"\|,/<>?`
    - Allowed: hyphens, periods (for specific uses)
    - Rationale: Ensures cross-platform compatibility and URL-friendliness
- **Domain-Specific Conventions**: Apply specialised knowledge for certain file types
    - Design assets follow industry standards where applicable
    - Development files respect language-specific conventions
    - Screenshots employ consistent descriptive patterning
    - Rationale: Balance system-wide consistency with domain best practices

## 10. Maintenance and Governance

To ensure long-term sustainability, the system will be maintained through:

- **Weekly Reviews**: Brief checks of recently created files
- **Monthly Audits**: Sample testing of system effectiveness
- **Quarterly Refinements**: Updates to standards based on experience
- **Continuous Documentation**: Tracking of challenges and solutions

## 11. Communication and Documentation

The project will maintain clear communication through:

- **Centralised Documentation**: Single source of truth for all standards
- **Version Control**: Tracking of all document changes
- **Cross-Referencing**: Linking between related documents
- **Clear Examples**: Practical illustrations of principles in action

---

_Version History:_

- v01 - 2025-01-28: Initial charter created
- v02 - 2025-02-28: Enhanced scope definition, stakeholders, methodology, and success criteria sections. Added Project Structure section.
- v03 - 2025-03-30: Updated project achievements, revised timeline completions, documented expanded automation tools, and added current status metrics.
