<filename>fomo-term-DICTIONARY-v01.md</filename>

# FOMO Term Dictionary v01

Part of the FOMO Controlled Vocabulary system:

- [Framework Document](https://github.com/exlennis/fomo-system/fomo-controlled-VOCABULARY-v02.md)
- [Term Dictionary](https://github.com/exlennis/fomo-system/fomo-term-DICTIONARY-v01.md) (this document)
- [Design Extensions](https://github.com/exlennis/fomo-system/fomo-vocabulary-EXTENSIONS-design-v01.md)
- [Development Extensions](https://github.com/exlennis/fomo-system/fomo-vocabulary-EXTENSIONS-development-v01.md)
- [Implementation Guide](https://github.com/exlennis/fomo-system/fomo-vocabulary-IMPLEMENTATION-GUIDE-v01.md)
- [Term Cheatsheet](https://github.com/exlennis/fomo-system/fomo-term-CHEATSHEET-v01.md)

## 1. Introduction

This Term Dictionary serves as the authoritative reference for all approved terms in the FOMO (File Organisation, Management & Optimisation) system. It provides standardised terminology for naming directories, files, tags, and other elements to ensure consistency across your digital environment.

### 1.1 How to Use This Dictionary

- **Finding Terms**: Browse alphabetically or use search functionality
- **Understanding Entries**: Each term includes definition, category, priority level, examples, and related terms
- **Priority Levels**: Terms are marked as essential (•••), important (••), or specialised (•)
- **Implementation**: See the [Implementation Guide](https://github.com/exlennis/fomo-system/fomo-vocabulary-IMPLEMENTATION-GUIDE-v01.md) for practical application
- **Domain Extensions**: For field-specific usage, see the relevant extension document

### 1.2 Term Categories

Terms are classified into six main categories:

|  Category |  Description |  Example Terms |  
| ---- | ---- | ----  |
|  Project |  Work creation and delivery |  design, dev, client |  
|  Resource |  Materials supporting projects |  assets, templates, fonts |  
|  Knowledge |  Information management |  docs, notes, research |  
|  System |  Computer configuration |  configs, scripts, search |  
|  Status/Workflow |  Process state indicators |  draft, approved, review |  
|  Temporal/Versioning |  Time or version identifiers |  current, v01, YYYYMMDD | 

## 2. Alphabetical Term Listing

### A

#### active

- **Definition**: Currently being worked on or in current use
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `project-proposal-active.docx`, `#active`
- **Usage Context**: Indicates an item requiring ongoing attention or currently in use
- **Related Terms**: current, ongoing, in-progress

#### app

- **Definition**: Application-focused development project or output
- **Category**: Project
- **Priority**: •• (Important)
- **Format Example**: `~/Projects/dev/client-app/`, `app-mockup-v01.sketch`
- **Usage Context**: Identifies mobile or desktop application projects
- **Related Terms**: mobile, desktop, development

#### approved

- **Definition**: Signed off by client or team
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `logo-design-approved-v02.ai`, `#approved`
- **Usage Context**: Indicates content that has received formal approval
- **Related Terms**: final, accepted, confirmed

#### archive

- **Definition**: Historical content preserved for record-keeping
- **Category**: Project, Temporal
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/archive/`, `#archive`
- **Usage Context**: Designates completed work kept for reference
- **Related Terms**: completed, historical, inactive

#### assets

- **Definition**: Design elements and media supporting creative work
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/assets/`, `project-assets-v01.zip`
- **Usage Context**: Categorises reusable design components
- **Related Terms**: elements, resources, media

#### automation

- **Definition**: Tools and workflows for automated processes
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/automation/`, `automation-scripts-v01.zip`
- **Usage Context**: Identifies scripts and configurations for automation
- **Related Terms**: scripts, workflows, tools

### B

#### backup

- **Definition**: System and data protection resources
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/backup/`, `backup-config-20250301.json`
- **Usage Context**: Identifies backup-related content and procedures
- **Related Terms**: archive, protection, recovery

#### bak

- **Definition**: Backup file prefix
- **Category**: System, Temporal
- **Priority**: •• (Important)
- **Format Example**: `bak-website-config-20250301.json`
- **Usage Context**: Identifies manually created backup files
- **Related Terms**: backup, archive, copy

#### brief

- **Definition**: Project specifications and requirements
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `project-brief-v01.pdf`, `#brief`
- **Usage Context**: Identifies initial project documentation
- **Related Terms**: specifications, requirements, outline

### C

#### catalogues

- **Definition**: Organisational systems for managing resources
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `~/Resources/catalogues/`, `font-catalogue-v01.json`
- **Usage Context**: Identifies metadata and organisational structures
- **Related Terms**: libraries, collections, management

#### client

- **Definition**: Work commissioned by external entities
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/design/client/`, `client-proposal-v01.pdf`, `#client`
- **Usage Context**: Identifies client-specific content
- **Related Terms**: commercial, commissioned, external

#### collaboration

- **Definition**: Projects involving multiple contributors
- **Category**: Project
- **Priority**: •• (Important)
- **Format Example**: `~/Projects/collaboration/`, `#collaboration`
- **Usage Context**: Identifies team-based work
- **Related Terms**: team, shared, partnership

#### complete

- **Definition**: Finished and verified work
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `project-complete.md`, `#complete`
- **Usage Context**: Indicates completion status
- **Related Terms**: finished, done, completed

#### configs

- **Definition**: Configuration files and settings
- **Category**: System
- **Priority**: ••• (Essential)
- **Format Example**: `~/System/configs/`, `app-configs-v01.json`
- **Usage Context**: Identifies system configuration content
- **Related Terms**: settings, preferences, parameters

#### content

- **Definition**: Text, media, or information for publication
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `website-content-v01.docx`, `#content`
- **Usage Context**: Identifies publishable material
- **Related Terms**: copy, text, information

#### current

- **Definition**: In active use or present state
- **Category**: Temporal
- **Priority**: ••• (Essential)
- **Format Example**: `current-portfolio.pdf`, `#current`
- **Usage Context**: Indicates currently relevant content
- **Related Terms**: active, present, now

### D

#### design

- **Definition**: Design-focused project work
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/design/`, `design-system-v01.sketch`, `#design`
- **Usage Context**: Identifies visual and interactive design projects
- **Related Terms**: visual, creative, artistic

#### desktop

- **Definition**: Computer-specific implementation
- **Category**: Project
- **Priority**: • (Specialised)
- **Format Example**: `app-desktop-v01.sketch`, `#desktop`
- **Usage Context**: Identifies desktop platform content
- **Related Terms**: computer, laptop, pc

#### dev

- **Definition**: Development-focused project work
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/dev/`, `dev-documentation-v01.md`, `#dev`
- **Usage Context**: Identifies programming and coding projects
- **Related Terms**: code, programming, engineering

#### docs

- **Definition**: Formal documentation and structured information
- **Category**: Knowledge
- **Priority**: ••• (Essential)
- **Format Example**: `~/Knowledge/docs/`, `api-docs-v01.md`, `#docs`
- **Usage Context**: Identifies instructional or explanatory content
- **Related Terms**: documentation, manuals, instructions

#### draft

- **Definition**: Initial or work-in-progress version
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `proposal-draft-v01.docx`, `#draft`
- **Usage Context**: Indicates draft status in a workflow
- **Related Terms**: in-progress, working, preliminary

### E

#### education

- **Definition**: Learning-focused projects and materials
- **Category**: Project
- **Priority**: •• (Important)
- **Format Example**: `~/Projects/education/`, `course-materials-v01.pdf`, `#education`
- **Usage Context**: Identifies educational content
- **Related Terms**: learning, training, courses

#### export

- **Definition**: Content formatted for external use
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `design-export-20250301.pdf`, `#export`
- **Usage Context**: Identifies exported deliverables
- **Related Terms**: output, deliverable, publication

### F

#### feedback

- **Definition**: Commentary and input on work
- **Category**: Status/Workflow
- **Priority**: •• (Important)
- **Format Example**: `design-feedback-20250301.md`, `#feedback`
- **Usage Context**: Identifies response to shared work
- **Related Terms**: comments, critique, review

#### final

- **Definition**: Completed and ready for delivery
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `logo-final-v03.ai`, `#final`
- **Usage Context**: Indicates final status in a workflow
- **Related Terms**: approved, complete, finished

#### fonts

- **Definition**: Typography resources
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/assets/fonts/`, `project-fonts-v01.zip`, `#fonts`
- **Usage Context**: Identifies font files and related content
- **Related Terms**: typography, type, lettering

### G

#### guides

- **Definition**: Instructional materials with procedures
- **Category**: Knowledge
- **Priority**: •• (Important)
- **Format Example**: `~/Knowledge/guides/`, `setup-guide-v01.md`, `#guide`
- **Usage Context**: Identifies step-by-step guidance
- **Related Terms**: instructions, tutorials, walkthroughs

### H

#### handoff

- **Definition**: Work prepared for transfer between disciplines
- **Category**: Project, Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `design-handoff-v01.sketch`, `#handoff`
- **Usage Context**: Identifies handoff documentation
- **Related Terms**: delivery, transfer, assets

### I

#### icons

- **Definition**: Symbolic visual elements for interfaces
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/assets/icons/`, `app-icons-v01.svg`, `#icons`
- **Usage Context**: Identifies icon files and collections
- **Related Terms**: symbols, glyphs, pictograms

#### images

- **Definition**: Visual content including photos and graphics
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/assets/images/`, `product-images-v01.zip`, `#images`
- **Usage Context**: Identifies image files and collections
- **Related Terms**: photos, pictures, graphics

#### inspirations

- **Definition**: Creative examples and influences
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `~/Resources/inspirations/`, `#inspiration`
- **Usage Context**: Identifies reference materials for creative direction
- **Related Terms**: examples, influences, moodboards

#### integration

- **Definition**: Connection points between different systems
- **Category**: System
- **Priority**: • (Specialised)
- **Format Example**: `~/System/integration/`, `api-integration-v01.js`, `#integration`
- **Usage Context**: Identifies integration-related content
- **Related Terms**: connection, linking, interface

### J

#### journal

- **Definition**: Time-based entries and reflections
- **Category**: Knowledge
- **Priority**: •• (Important)
- **Format Example**: `~/Knowledge/journal/`, `project-journal-202503.md`, `#journal`
- **Usage Context**: Identifies chronological personal content
- **Related Terms**: diary, log, notes

### K

#### knowledge

- **Definition**: Information collection and management
- **Category**: Knowledge
- **Priority**: ••• (Essential)
- **Format Example**: `~/Knowledge/`, `knowledge-base-v01.md`, `#knowledge`
- **Usage Context**: Identifies knowledge-related content
- **Related Terms**: information, learning, wisdom

### L

#### learning

- **Definition**: Educational resources and study materials
- **Category**: Knowledge
- **Priority**: •• (Important)
- **Format Example**: `~/Knowledge/learning/`, `python-learning-v01.md`, `#learning`
- **Usage Context**: Identifies learning-focused content
- **Related Terms**: education, study, training

#### legacy

- **Definition**: Outdated but preserved for reference
- **Category**: Temporal
- **Priority**: •• (Important)
- **Format Example**: `legacy-website-archive.zip`, `#legacy`
- **Usage Context**: Identifies historical content
- **Related Terms**: old, archived, historical

#### libraries

- **Definition**: Collections of related resources
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `~/Resources/libraries/`, `code-libraries-v01.zip`, `#libraries`
- **Usage Context**: Identifies organised collections
- **Related Terms**: collections, repositories, archives

#### logs

- **Definition**: Records of system activities and events
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/logs/`, `system-logs-202503.txt`, `#logs`
- **Usage Context**: Identifies logging information
- **Related Terms**: records, history, tracking

### M

#### maintenance

- **Definition**: System upkeep and optimisation resources
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/maintenance/`, `app-maintenance-v01.sh`, `#maintenance`
- **Usage Context**: Identifies maintenance-related content
- **Related Terms**: upkeep, optimisation, cleanup

#### meeting

- **Definition**: Discussion session documentation
- **Category**: Project, Knowledge
- **Priority**: •• (Important)
- **Format Example**: `meeting-notes-20250301.md`, `#meeting`
- **Usage Context**: Identifies meeting-related content
- **Related Terms**: discussion, conference, session

#### mobile

- **Definition**: Mobile device implementation
- **Category**: Project
- **Priority**: • (Specialised)
- **Format Example**: `app-mobile-prototype-v01.fig`, `#mobile`
- **Usage Context**: Identifies mobile platform content
- **Related Terms**: phone, tablet, portable

#### mockups

- **Definition**: Visual representations of designs
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/mockups/`, `website-mockup-v01.sketch`, `#mockup`
- **Usage Context**: Identifies mockup files
- **Related Terms**: comps, renderings, visuals

### N

#### notes

- **Definition**: Personal information and insights
- **Category**: Knowledge
- **Priority**: ••• (Essential)
- **Format Example**: `~/Knowledge/notes/`, `project-notes-20250301.md`, `#notes`
- **Usage Context**: Identifies informal documentation
- **Related Terms**: thoughts, ideas, observations

### O

#### old

- **Definition**: Previous version superseded by newer content
- **Category**: Temporal
- **Priority**: •• (Important)
- **Format Example**: `old-logo-archive.zip`, `#old`
- **Usage Context**: Identifies outdated content
- **Related Terms**: previous, outdated, superseded

### P

#### patterns

- **Definition**: Reusable design or code patterns
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `~/Resources/patterns/`, `ui-patterns-v01.sketch`, `#patterns`
- **Usage Context**: Identifies pattern libraries and examples
- **Related Terms**: components, elements, templates

#### personal

- **Definition**: Self-initiated creative or technical work
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/personal/`, `personal-website-v01.sketch`, `#personal`
- **Usage Context**: Identifies non-client work
- **Related Terms**: own, individual, private

#### presentation

- **Definition**: Content formatted for presenting to others
- **Category**: Resource
- **Priority**: •• (Important)
- **Format Example**: `client-presentation-20250301.pptx`, `#presentation`
- **Usage Context**: Identifies presentation materials
- **Related Terms**: slides, deck, slideshow

#### production

- **Definition**: Assets ready for implementation
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/design/client/production/`, `website-production-v01.zip`, `#production`
- **Usage Context**: Identifies production-ready content
- **Related Terms**: implementation, deployment, delivery

#### projects

- **Definition**: Container for active creation work
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `~/Projects/`, `projects-overview.md`, `#project`
- **Usage Context**: Identifies project-related content
- **Related Terms**: works, creations, activities

#### proposal

- **Definition**: Preliminary project concepts and pitches
- **Category**: Project
- **Priority**: ••• (Essential)
- **Format Example**: `client-proposal-20250301.pdf`, `#proposal`
- **Usage Context**: Identifies proposed work
- **Related Terms**: pitch, concept, plan

#### prototype

- **Definition**: Early-stage functional or visual demonstrations
- **Category**: Project, Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `app-prototype-v01.fig`, `#prototype`
- **Usage Context**: Identifies prototype content
- **Related Terms**: demo, proof-of-concept, test

### Q

#### quarterly

- **Definition**: Three-month cycle designation
- **Category**: Temporal
- **Priority**: • (Specialised)
- **Format Example**: `report-quarterly-202501.pdf`, `#quarterly`
- **Usage Context**: Identifies quarterly content
- **Related Terms**: q1, q2, q3, q4

### R

#### reference

- **Definition**: Authoritative sources and materials
- **Category**: Knowledge, Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/reference/`, `design-reference-v01.pdf`, `#reference`
- **Usage Context**: Identifies reference content
- **Related Terms**: sources, documentation, guides

#### rejected

- **Definition**: Not accepted in current form
- **Category**: Status/Workflow
- **Priority**: •• (Important)
- **Format Example**: `logo-rejected-v01.ai`, `#rejected`
- **Usage Context**: Indicates rejection status
- **Related Terms**: declined, not-approved, refused

#### research

- **Definition**: Collected information for analysis
- **Category**: Knowledge
- **Priority**: ••• (Essential)
- **Format Example**: `~/Knowledge/research/`, `market-research-v01.pdf`, `#research`
- **Usage Context**: Identifies research materials
- **Related Terms**: analysis, investigation, study

#### resources

- **Definition**: Supportive materials used across projects
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/`, `resources-overview.md`, `#resources`
- **Usage Context**: Identifies resource content
- **Related Terms**: assets, materials, supplies

#### review

- **Definition**: Ready for feedback or evaluation
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `design-review-v02.sketch`, `#review`
- **Usage Context**: Indicates review status
- **Related Terms**: evaluate, assess, feedback

#### revision

- **Definition**: Updated based on feedback
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `proposal-revision-v02.docx`, `#revision`
- **Usage Context**: Indicates revision status
- **Related Terms**: updated, modified, changed

### S

#### scripts

- **Definition**: Automation code and utilities
- **Category**: System
- **Priority**: ••• (Essential)
- **Format Example**: `~/System/scripts/`, `rename-scripts-v01.sh`, `#scripts`
- **Usage Context**: Identifies scripting content
- **Related Terms**: code, automation, programming

#### search

- **Definition**: Saved searches and smart folders
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/search/`, `client-search-v01.savedSearch`, `#search`
- **Usage Context**: Identifies search configurations
- **Related Terms**: find, query, lookup

#### security

- **Definition**: Protection and privacy-related components
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/security/`, `security-config-v01.json`, `#security`
- **Usage Context**: Identifies security content
- **Related Terms**: protection, privacy, safety

#### system

- **Definition**: Computer configuration and management
- **Category**: System
- **Priority**: ••• (Essential)
- **Format Example**: `~/System/`, `system-overview.md`, `#system`
- **Usage Context**: Identifies system-related content
- **Related Terms**: configuration, management, setup

### T

#### templates

- **Definition**: Starting points and frameworks for new work
- **Category**: Resource
- **Priority**: ••• (Essential)
- **Format Example**: `~/Resources/templates/`, `invoice-template-v01.docx`, `#template`
- **Usage Context**: Identifies template content
- **Related Terms**: boilerplate, starter, framework

#### tmp

- **Definition**: Temporary file prefix
- **Category**: Temporal
- **Priority**: •• (Important)
- **Format Example**: `tmp-export-20250301.csv`, `#tmp`
- **Usage Context**: Identifies temporary content
- **Related Terms**: temporary, interim, transient

#### todo

- **Definition**: Requires action or attention
- **Category**: Status/Workflow
- **Priority**: ••• (Essential)
- **Format Example**: `project-todo-20250301.md`, `#todo`
- **Usage Context**: Indicates action needed
- **Related Terms**: action, task, pending

### U

#### utilities

- **Definition**: Helper applications and tools
- **Category**: System
- **Priority**: •• (Important)
- **Format Example**: `~/System/utilities/`, `conversion-utility-v01.sh`, `#utility`
- **Usage Context**: Identifies utility content
- **Related Terms**: tools, helpers, aids

### V

#### v##

- **Definition**: Version number with leading zeros
- **Category**: Temporal/Versioning
- **Priority**: ••• (Essential)
- **Format Example**: `logo-v01.ai`, `report-v02.pdf`
- **Usage Context**: Indicates version
- **Related Terms**: version, revision, iteration

#### vault

- **Definition**: Personal knowledge management system
- **Category**: Knowledge
- **Priority**: ••• (Essential)
- **Format Example**: `~/Knowledge/vault/`, `#vault`
- **Usage Context**: Identifies knowledge base location
- **Related Terms**: database, repository, knowledge-base

### W

#### waiting

- **Definition**: Pending external input
- **Category**: Status/Workflow
- **Priority**: •• (Important)
- **Format Example**: `project-waiting-feedback.md`, `#waiting`
- **Usage Context**: Indicates waiting status
- **Related Terms**: pending, on-hold, standby

#### web

- **Definition**: Web-based project or platform
- **Category**: Project
- **Priority**: •• (Important)
- **Format Example**: `~/Projects/dev/web-application/`, `website-mockup-v01.sketch`, `#web`
- **Usage Context**: Identifies web-related content
- **Related Terms**: website, online, internet

#### wiki

- **Definition**: Interconnected knowledge repository
- **Category**: Knowledge
- **Priority**: •• (Important)
- **Format Example**: `~/Knowledge/wiki/`, `project-wiki-v01.md`, `#wiki`
- **Usage Context**: Identifies wiki content
- **Related Terms**: knowledge-base, documentation, reference

### Y

#### YYYYMMDD

- **Definition**: Date in ISO 8601 format
- **Category**: Temporal/Versioning
- **Priority**: ••• (Essential)
- **Format Example**: `meeting-notes-20250301.md`, `invoice-20250315.pdf`
- **Usage Context**: Indicates date in standardised format
- **Related Terms**: date, ISO-date, calendar

## 3. Category-Based Term Reference

For category-based term groupings, specific usage guidance, and domain-specific applications, see:

- [Framework Document](https://github.com/exlennis/fomo-system/fomo-controlled-VOCABULARY-v02.md) for organisation and principles
- [Design Extensions](https://github.com/exlennis/fomo-system/fomo-vocabulary-EXTENSIONS-design-v01.md) for design-specific terms
- [Development Extensions](https://github.com/exlennis/fomo-system/fomo-vocabulary-EXTENSIONS-development-v01.md) for development-specific terms

## 4. Implementation Notes

For practical application of these terms, see the [Implementation Guide](https://github.com/exlennis/fomo-system/fomo-vocabulary-IMPLEMENTATION-GUIDE-v01.md). For a quick reference of essential terms, see the [Term Cheatsheet](https://github.com/exlennis/fomo-system/fomo-term-CHEATSHEET-v01.md).

## 5. Integration with FOMO Documents

This Term Dictionary document works in conjunction with other FOMO project documents to form a unified system:

- **fomo-project-charter-v##.md**: Establishes the overall vision and principles for the fomo system
- **fomo-naming-standards-v##.md**: Defines the file naming conventions used within this structure
- **fomo-directory-structure-v##.md**: Defines the folder hierarchy these named files will live within
- **fomo-controlled-vocabulary-v##.md**: Standardised terms for consistent folder naming
- **fomo-implementation-plan-v##.md**: Details the step-by-step approach for system deployment
- **fomo-??? workflow-configurations-v##.md**: Detailed automation setup for file management
- **fomo-special-cases-v##.md**: Provides guidance for exceptions to the standard structure
- **fomo-??? Naming-Cheatsheet-v01.md**: Quick reference guide for daily application
- **fomo-maintenance-log-v##.md**: Tracks changes and issues encountered during implementation


* * *

_Version History:_

- v01 - 2025-04-10: Initial term dictionary created from comprehensive term extracts
