# FOMO Controlled Vocabulary v01

## 1. Introduction

### 1.1 Purpose and Benefits

This controlled vocabulary provides a standardised set of terms for the File Organisation, Management & Optimisation (FOMO) project. It serves as the authoritative reference for naming directories, folders, files, tags, and other elements within the system. 

Implementing this controlled vocabulary offers significant benefits:

- **Consistency**: Ensures uniform naming across projects, resources, and systems
- **Reduced Cognitive Load**: Eliminates decision fatigue when naming files and folders
- **Enhanced Searchability**: Improves finding capabilities through predictable terminology
- **Automation Support**: Enables reliable script-based file processing and organisation
- **Cross-Platform Compatibility**: Maintains consistency across different tools and services
- **Collaboration Efficiency**: Creates a shared language for file exchange and handoffs
- **System Integrity**: Preserves the logical structure of the FOMO system over time
- **Scalability**: Provides a framework that can grow with evolving needs

### 1.2 Implementation Overview

This controlled vocabulary follows a `flat with controlled combinations` approach:

- **Core Terms**: A concise set of single-word base terms form the foundation
- **Combinations**: Terms can be combined using hyphens to create more specific descriptors
- **Contextual Application**: The same term may appear differently based on its level in the directory structure (e.g., capitalised at top level, lowercase with hyphens at nested levels)
- **Progressive Implementation**: The vocabulary should be applied first to new files and active projects, then gradually extended to historical content
- **Living Document**: This vocabulary will evolve through documented updates as usage patterns emerge and new needs are identified

## 2. Core Terminology Categories

### 2.1 Project-Related Terms

Project-related terms describe work that involves creating, modifying, or delivering specific outcomes. These terms appear primarily within the Projects directory structure.

**Primary Terms:**
- **design**: Design-focused project work (visual, interactive, experiential)
- **dev**: Development-focused project work (coding, programming, automation)
- **client**: Work commissioned by external entities
- **personal**: Self-initiated creative or technical work
- **education**: Learning-focused projects, courses, and assignments
- **archive**: Completed projects maintained for reference
- **collaboration**: Projects involving multiple contributors
- **proposal**: Preliminary project concepts and pitches
- **prototype**: Early-stage functional or visual demonstrations
- **handoff**: Work prepared for transfer between disciplines

### 2.2 Resource-Related Terms

Resource-related terms describe supportive materials used across projects. These terms appear primarily within the Resources directory structure.

**Primary Terms:**
- **assets**: Design elements and media files supporting creative work
- **templates**: Starting points and frameworks for new work
- **references**: Informational materials consulted during projects
- **inspirations**: Creative examples and influences
- **fonts**: Typography resources organised by family and style
- **icons**: Symbolic visual elements used in interfaces
- **patterns**: Reusable design or code patterns
- **catalogues**: Organisational systems for managing resources
- **libraries**: Collections of related resources with common attributes
- **mockups**: Templates for presenting designs in context

### 2.3 Knowledge-Related Terms

Knowledge-related terms describe information collection and management. These terms appear primarily within the Knowledge directory structure.

**Primary Terms:**
- **docs**: Formal documentation and structured information
- **notes**: Personal information and insights
- **research**: Collected information for analysis and reference
- **vault**: Personal knowledge management system
- **journal**: Time-based entries and reflections
- **guides**: Instructional materials with step-by-step procedures
- **wiki**: Interconnected knowledge repository
- **reference**: Authoritative sources and materials
- **learning**: Educational resources and study materials
- **cheatsheet**: Concise reference guides for quick consultation

### 2.4 System-Related Terms

System-related terms describe computer configuration and management. These terms appear primarily within the System directory structure.

**Primary Terms:**
- **configs**: Configuration files and settings
- **scripts**: Automation code and utilities
- **search**: Saved searches and smart folders
- **backup**: System and data protection resources
- **automation**: Tools and workflows for automated processes
- **maintenance**: System upkeep and optimisation resources
- **security**: Protection and privacy-related components
- **logs**: Records of system activities and events
- **utilities**: Helper applications and tools
- **integration**: Connection points between different systems

### 2.5 Temporal/Versioning Terms

Temporal/versioning terms indicate time relationships or version control. These terms may appear as prefixes or suffixes in filenames or as directory markers.

**Primary Terms:**
- **current**: In active use or present state
- **legacy**: Outdated but preserved for reference
- **archive**: Historical content preserved for record-keeping
- **v##**: Version number with leading zeros (e.g., v01, v02)
- **YYYYMMDD**: Date in ISO 8601 format
- **old**: Previous version superseded by newer content
- **new**: Recently created or updated content
- **interim**: Temporary or transitional state
- **quarterly**: Three-month cycle designation
- **annual**: Yearly cycle designation

### 2.6 Status/Workflow Terms

Status/workflow terms indicate state or stage in processes. These terms typically appear as suffixes in filenames or as metadata tags.

**Primary Terms:**
- **draft**: Initial or work-in-progress version
- **review**: Ready for feedback or evaluation
- **approved**: Signed off by client or team
- **rejected**: Not accepted in current form
- **revision**: Updated based on feedback
- **final**: Completed and ready for delivery
- **active**: Currently being worked on
- **todo**: Requires action or attention
- **waiting**: Pending external input
- **complete**: Finished and verified

## 3. Term Formatting Standards

### 3.1 Directory/Folder Terminology

#### 3.1.1 Top-Level Folders (Level 1)

Top-level folders follow macOS conventions with capitalisation:

- Use single-word names with initial capital letter
- Examples: Projects, Resources, Knowledge, System
- Restricted to the core organisational categories

```
~/Projects/        # Container for active work
~/Resources/       # Supportive materials used across projects
~/Knowledge/       # Information collection and management
~/System/          # Computer configuration and management
```

#### 3.1.2 Nested Folders (Level 2+)

Nested folders use kebab-case:

- Lowercase letters only
- Single words preferred
- Hyphen separators for compound terms
- Avoid spaces, underscores, or special characters
- Maximum of 2-3 hyphens in a folder name for readability

```
~/Projects/dev/web-application/
~/Resources/assets/client-logos/
~/Knowledge/notes/project-ideas/
~/System/scripts/file-renaming/
```

### 3.2 File Terminology

File naming follows kebab-case with additional elements:

- Lowercase letters for descriptive portions
- Hyphens between words
- May include:
  - Project identifiers
  - Content descriptors
  - Date information (YYYYMMDD)
  - Status indicators
  - Version numbers (v##)
- File extension appropriate to file type

**Pattern examples**:
```
project-report-20250301-v02.pdf
client-logo-primary-v01.svg
meeting-notes-quarterly-20250315.md
```

### 3.3 Tag Terminology

Tags use a flat controlled vocabulary with system-specific formatting:

- Single-word tags preferred 
- Lowercase with no spaces
- Same core terminology as directories and files
- Applied individually rather than as compound terms
- May be prefixed with # symbol in some applications
- Combined through co-occurrence rather than concatenation

**Example tag sets**:

    ```
    #client #logo #approved
    #project #proposal #draft
    #resource #font #serif
    ```

### 3.4 Special Case Terminology

#### 3.4.1 Font Files

Font files follow typography industry standards:

- PascalCase for font family names
- Hyphen before style name
- Style name uses PascalCase
- Examples: SourceSansPro-Regular.ttf, RobotoFlex-Bold.otf

#### 3.4.2 Development Files

Development files follow language-specific conventions when required:

- React components use PascalCase (e.g., ButtonGroup.tsx)
- Python modules use snake_case (e.g., database_connector.py)
- Configuration files use established conventions (e.g., .env-production)

#### 3.4.3 Export Variations

Exported assets with variations use specific indicators:

- Resolution/density indicated with underscore: logo_2x.png
- Colour variants use descriptive suffix: logo-dark.svg, logo-light.svg
- Size variants use descriptive size terms: icon-small.png, icon-large.png

### 3.5 Prohibited Terminology

To maintain system integrity, avoid these naming practices:

- **No spaces** in directory or file names (use hyphens instead)
- **No special characters** except those explicitly allowed: hyphens, periods, underscores in specific contexts
- **No generic descriptors** without context: "misc", "stuff", "things", "temp" (unless part of a structured workflow)
- **No ambiguous abbreviations**: Use established abbreviations only (PDF, PNG, etc.)
- **No emoji or special unicode characters** in filenames or directories
- **No case mixing** except where specified for special cases (e.g., font files)
- **No overly generic terms** as standalone folders: "files", "docs", "images" (without additional context)

## 4. Implementation Guidelines

### 4.1 When to Use Controlled Terms

Apply controlled vocabulary terms in these contexts:

- **Creating new directories**: Always use controlled terms for structure
- **Saving new files**: Apply appropriate naming patterns with controlled terms
- **Tagging content**: Use consistent tag terminology across platforms
- **Developing automation**: Refer to controlled terms in scripts and rules
- **Creating templates**: Embed controlled vocabulary in template names
- **Writing documentation**: Use consistent terminology in all documentation
- **Setting up project structures**: Apply directory patterns with controlled terms

Prioritise implementation in this order:
1. New file creation and saving
2. Active project reorganisation
3. Resources and knowledge management
4. System configuration
5. Historical content (as resources permit)

### 4.2 How to Combine Terms

Build complex descriptors by combining terms following these principles:

- **Logical ordering**: Use the pattern [context]-[type]-[descriptor]-[metadata]
- **Minimal combinations**: Use only as many terms as needed for clarity
- **Consistent separators**: Always use hyphens between combined terms
- **Limited depth**: Aim for 2-3 hyphenated components maximum
- **Natural language flow**: Arrange terms for human readability

**Examples**:
- For a client proposal document: `client-proposal-project-20250301.pdf`
- For a logo design: `logo-primary-v02.svg`
- For meeting notes: `meeting-notes-quarterly-20250315.md`

### 4.3 Handling Special Cases

Special cases require specific approaches:

#### 4.3.1 Multilingual Content

For content available in multiple languages:
- Add ISO 639-1 language code before the extension
- Examples: `user-manual.en.pdf`, `user-manual.fr.pdf`

#### 4.3.2 Temporary Files

For temporary working files:
- Prefix with `tmp-` to indicate temporary status
- Include date for automatic cleanup reference
- Example: `tmp-export-20250301.csv`

#### 4.3.3 Backup Files

For manual backups:
- Prefix with `bak-` to indicate backup status
- Include date of backup creation
- Example: `bak-website-config-20250301.json`

#### 4.3.4 Client-Specific Variations

For client-specific naming requirements:
- Document exceptions in the maintenance log
- Create client-specific automation rules where needed
- Follow client conventions for deliverables while maintaining internal standards for working files

### 4.4 Extending the Vocabulary

The controlled vocabulary can evolve through this process:

1. **Identify need**: Recognise when existing terms don't adequately describe content
2. **Check alternatives**: Verify no existing term combinations can serve the purpose
3. **Propose addition**: Suggest new term following formatting standards
4. **Document addition**: Add to controlled vocabulary with definition, usage examples
5. **Update automation**: Modify any automation rules to accommodate new term
6. **Review periodically**: Assess term usage and value quarterly

Criteria for adding new terms:
- Fills a genuine semantic gap
- Consistent with existing terminology patterns
- Clear, concise, and descriptive
- Useful across multiple contexts
- Supports automation goals

## 5. Term Dictionary

This alphabetically ordered master list includes all approved terms with definitions, purpose, usage examples, and related terms.

### A

**active**
- Definition: Currently being worked on or in current use
- Purpose: Indicates active status in a workflow
- Usage: `project-proposal-active.docx`, `#active`
- Related Terms: current, ongoing, in-progress

**app**
- Definition: Application-focused development project or output
- Purpose: Identifies mobile or desktop application projects
- Usage: `~/Projects/dev/client-app/`, `app-mockup-v01.sketch`
- Related Terms: mobile, desktop, development

**approved**
- Definition: Signed off by client or team
- Purpose: Indicates approval status in a workflow
- Usage: `logo-design-approved-v02.ai`, `#approved`
- Related Terms: final, accepted, confirmed

**archive**
- Definition: Historical content preserved for record-keeping
- Purpose: Designates completed work kept for reference
- Usage: `~/Projects/archive/`, `#archive`
- Related Terms: completed, historical, inactive

**assets**
- Definition: Design elements and media supporting creative work
- Purpose: Categorises reusable design components
- Usage: `~/Resources/assets/`, `project-assets-v01.zip`
- Related Terms: elements, resources, media

**automation**
- Definition: Tools and workflows for automated processes
- Purpose: Identifies scripts and configurations for automation
- Usage: `~/System/automation/`, `automation-scripts-v01.zip`
- Related Terms: scripts, workflows, tools

### B

**backup**
- Definition: System and data protection resources
- Purpose: Identifies backup-related content
- Usage: `~/System/backup/`, `backup-config-20250301.json`
- Related Terms: archive, protection, recovery

**bak**
- Definition: Backup file prefix
- Purpose: Identifies manually created backup files
- Usage: `bak-website-config-20250301.json`
- Related Terms: backup, archive, copy

**brief**
- Definition: Project specifications and requirements
- Purpose: Identifies initial project documentation
- Usage: `project-brief-v01.pdf`, `#brief`
- Related Terms: specifications, requirements, outline

### C

**catalogues**
- Definition: Organisational systems for managing resources
- Purpose: Identifies metadata and organisational structures
- Usage: `~/Resources/catalogues/`, `font-catalogue-v01.json`
- Related Terms: libraries, collections, management

**client**
- Definition: Work commissioned by external entities
- Purpose: Identifies client-specific content
- Usage: `~/Projects/design/client/`, `client-proposal-v01.pdf`, `#client`
- Related Terms: commercial, commissioned, external

**collaboration**
- Definition: Projects involving multiple contributors
- Purpose: Identifies team-based work
- Usage: `~/Projects/collaboration/`, `#collaboration`
- Related Terms: team, shared, partnership

**complete**
- Definition: Finished and verified work
- Purpose: Indicates completion status
- Usage: `project-complete.md`, `#complete`
- Related Terms: finished, done, completed

**configs**
- Definition: Configuration files and settings
- Purpose: Identifies system configuration content
- Usage: `~/System/configs/`, `app-configs-v01.json`
- Related Terms: settings, preferences, parameters

**content**
- Definition: Text, media, or information for publication
- Purpose: Identifies publishable material
- Usage: `website-content-v01.docx`, `#content`
- Related Terms: copy, text, information

**current**
- Definition: In active use or present state
- Purpose: Indicates currently relevant content
- Usage: `current-portfolio.pdf`, `#current`
- Related Terms: active, present, now

### D

**design**
- Definition: Design-focused project work
- Purpose: Identifies visual and interactive design projects
- Usage: `~/Projects/design/`, `design-system-v01.sketch`, `#design`
- Related Terms: visual, creative, artistic

**desktop**
- Definition: Computer-specific implementation
- Purpose: Identifies desktop platform content
- Usage: `app-desktop-v01.sketch`, `#desktop`
- Related Terms: computer, laptop, pc

**dev**
- Definition: Development-focused project work
- Purpose: Identifies programming and coding projects
- Usage: `~/Projects/dev/`, `dev-documentation-v01.md`, `#dev`
- Related Terms: code, programming, engineering

**docs**
- Definition: Formal documentation and structured information
- Purpose: Identifies instructional or explanatory content
- Usage: `~/Knowledge/docs/`, `api-docs-v01.md`, `#docs`
- Related Terms: documentation, manuals, instructions

**draft**
- Definition: Initial or work-in-progress version
- Purpose: Indicates draft status in a workflow
- Usage: `proposal-draft-v01.docx`, `#draft`
- Related Terms: in-progress, working, preliminary

### E

**education**
- Definition: Learning-focused projects and materials
- Purpose: Identifies educational content
- Usage: `~/Projects/education/`, `course-materials-v01.pdf`, `#education`
- Related Terms: learning, training, courses

**export**
- Definition: Content formatted for external use
- Purpose: Identifies exported deliverables
- Usage: `design-export-20250301.pdf`, `#export`
- Related Terms: output, deliverable, publication

### F

**feedback**
- Definition: Commentary and input on work
- Purpose: Identifies response to shared work
- Usage: `design-feedback-20250301.md`, `#feedback`
- Related Terms: comments, critique, review

**final**
- Definition: Completed and ready for delivery
- Purpose: Indicates final status in a workflow
- Usage: `logo-final-v03.ai`, `#final`
- Related Terms: approved, complete, finished

**fonts**
- Definition: Typography resources
- Purpose: Identifies font files and related content
- Usage: `~/Resources/assets/fonts/`, `project-fonts-v01.zip`, `#fonts`
- Related Terms: typography, type, lettering

### G

**guides**
- Definition: Instructional materials with procedures
- Purpose: Identifies step-by-step guidance
- Usage: `~/Knowledge/guides/`, `setup-guide-v01.md`, `#guide`
- Related Terms: instructions, tutorials, walkthroughs

### H

**handoff**
- Definition: Work prepared for transfer between disciplines
- Purpose: Identifies handoff documentation
- Usage: `design-handoff-v01.sketch`, `#handoff`
- Related Terms: delivery, transfer, assets

### I

**icons**
- Definition: Symbolic visual elements for interfaces
- Purpose: Identifies icon files and collections
- Usage: `~/Resources/assets/icons/`, `app-icons-v01.svg`, `#icons`
- Related Terms: symbols, glyphs, pictograms

**images**
- Definition: Visual content including photos and graphics
- Purpose: Identifies image files and collections
- Usage: `~/Resources/assets/images/`, `product-images-v01.zip`, `#images`
- Related Terms: photos, pictures, graphics

**inspirations**
- Definition: Creative examples and influences
- Purpose: Identifies reference materials for creative direction
- Usage: `~/Resources/inspirations/`, `#inspiration`
- Related Terms: examples, influences, moodboards

**integration**
- Definition: Connection points between different systems
- Purpose: Identifies integration-related content
- Usage: `~/System/integration/`, `api-integration-v01.js`, `#integration`
- Related Terms: connection, linking, interface

### J

**journal**
- Definition: Time-based entries and reflections
- Purpose: Identifies chronological personal content
- Usage: `~/Knowledge/journal/`, `project-journal-202503.md`, `#journal`
- Related Terms: diary, log, notes

### K

**knowledge**
- Definition: Information collection and management
- Purpose: Identifies knowledge-related content
- Usage: `~/Knowledge/`, `knowledge-base-v01.md`, `#knowledge`
- Related Terms: information, learning, wisdom

### L

**learning**
- Definition: Educational resources and study materials
- Purpose: Identifies learning-focused content
- Usage: `~/Knowledge/learning/`, `python-learning-v01.md`, `#learning`
- Related Terms: education, study, training

**legacy**
- Definition: Outdated but preserved for reference
- Purpose: Identifies historical content
- Usage: `legacy-website-archive.zip`, `#legacy`
- Related Terms: old, archived, historical

**libraries**
- Definition: Collections of related resources
- Purpose: Identifies organised collections
- Usage: `~/Resources/libraries/`, `code-libraries-v01.zip`, `#libraries`
- Related Terms: collections, repositories, archives

**logs**
- Definition: Records of system activities and events
- Purpose: Identifies logging information
- Usage: `~/System/logs/`, `system-logs-202503.txt`, `#logs`
- Related Terms: records, history, tracking

### M

**maintenance**
- Definition: System upkeep and optimisation resources
- Purpose: Identifies maintenance-related content
- Usage: `~/System/maintenance/`, `app-maintenance-v01.sh`, `#maintenance`
- Related Terms: upkeep, optimisation, cleanup

**meeting**
- Definition: Discussion session documentation
- Purpose: Identifies meeting-related content
- Usage: `meeting-notes-20250301.md`, `#meeting`
- Related Terms: discussion, conference, session

**mobile**
- Definition: Mobile device implementation
- Purpose: Identifies mobile platform content
- Usage: `app-mobile-prototype-v01.fig`, `#mobile`
- Related Terms: phone, tablet, portable

**mockups**
- Definition: Visual representations of designs
- Purpose: Identifies mockup files
- Usage: `~/Resources/mockups/`, `website-mockup-v01.sketch`, `#mockup`
- Related Terms: comps, renderings, visuals

### N

**notes**
- Definition: Personal information and insights
- Purpose: Identifies informal documentation
- Usage: `~/Knowledge/notes/`, `project-notes-20250301.md`, `#notes`
- Related Terms: thoughts, ideas, observations

### O

**old**
- Definition: Previous version superseded by newer content
- Purpose: Identifies outdated content
- Usage: `old-logo-archive.zip`, `#old`
- Related Terms: previous, outdated, superseded

### P

**patterns**
- Definition: Reusable design or code patterns
- Purpose: Identifies pattern libraries and examples
- Usage: `~/Resources/patterns/`, `ui-patterns-v01.sketch`, `#patterns`
- Related Terms: components, elements, templates

**personal**
- Definition: Self-initiated creative or technical work
- Purpose: Identifies non-client work
- Usage: `~/Projects/personal/`, `personal-website-v01.sketch`, `#personal`
- Related Terms: own, individual, private

**presentation**
- Definition: Content formatted for presenting to others
- Purpose: Identifies presentation materials
- Usage: `client-presentation-20250301.pptx`, `#presentation`
- Related Terms: slides, deck, slideshow

**production**
- Definition: Assets ready for implementation
- Purpose: Identifies production-ready content
- Usage: `~/Projects/design/client/production/`, `website-production-v01.zip`, `#production`
- Related Terms: implementation, deployment, delivery

**projects**
- Definition: Container for active creation work
- Purpose: Identifies project-related content
- Usage: `~/Projects/`, `projects-overview.md`, `#project`
- Related Terms: works, creations, activities

**proposal**
- Definition: Preliminary project concepts and pitches
- Purpose: Identifies proposed work
- Usage: `client-proposal-20250301.pdf`, `#proposal`
- Related Terms: pitch, concept, plan

**prototype**
- Definition: Early-stage functional or visual demonstrations
- Purpose: Identifies prototype content
- Usage: `app-prototype-v01.fig`, `#prototype`
- Related Terms: demo, proof-of-concept, test

### Q

**quarterly**
- Definition: Three-month cycle designation
- Purpose: Identifies quarterly content
- Usage: `report-quarterly-202501.pdf`, `#quarterly`
- Related Terms: q1, q2, q3, q4

### R

**reference**
- Definition: Authoritative sources and materials
- Purpose: Identifies reference content
- Usage: `~/Resources/reference/`, `design-reference-v01.pdf`, `#reference`
- Related Terms: sources, documentation, guides

**rejected**
- Definition: Not accepted in current form
- Purpose: Indicates rejection status
- Usage: `logo-rejected-v01.ai`, `#rejected`
- Related Terms: declined, not-approved, refused

**research**
- Definition: Collected information for analysis
- Purpose: Identifies research materials
- Usage: `~/Knowledge/research/`, `market-research-v01.pdf`, `#research`
- Related Terms: analysis, investigation, study

**resources**
- Definition: Supportive materials used across projects
- Purpose: Identifies resource content
- Usage: `~/Resources/`, `resources-overview.md`, `#resources`
- Related Terms: assets, materials, supplies

**review**
- Definition: Ready for feedback or evaluation
- Purpose: Indicates review status
- Usage: `design-review-v02.sketch`, `#review`
- Related Terms: evaluate, assess, feedback

**revision**
- Definition: Updated based on feedback
- Purpose: Indicates revision status
- Usage: `proposal-revision-v02.docx`, `#revision`
- Related Terms: updated, modified, changed

### S

**scripts**
- Definition: Automation code and utilities
- Purpose: Identifies scripting content
- Usage: `~/System/scripts/`, `rename-scripts-v01.sh`, `#scripts`
- Related Terms: code, automation, programming

**search**
- Definition: Saved searches and smart folders
- Purpose: Identifies search configurations
- Usage: `~/System/search/`, `client-search-v01.savedSearch`, `#search`
- Related Terms: find, query, lookup

**security**
- Definition: Protection and privacy-related components
- Purpose: Identifies security content
- Usage: `~/System/security/`, `security-config-v01.json`, `#security`
- Related Terms: protection, privacy, safety

**system**
- Definition: Computer configuration and management
- Purpose: Identifies system-related content
- Usage: `~/System/`, `system-overview.md`, `#system`
- Related Terms: configuration, management, setup

### T

**templates**
- Definition: Starting points and frameworks for new work
- Purpose: Identifies template content
- Usage: `~/Resources/templates/`, `invoice-template-v01.docx`, `#template`
- Related Terms: boilerplate, starter, framework

**tmp**
- Definition: Temporary file prefix
- Purpose: Identifies temporary content
- Usage: `tmp-export-20250301.csv`, `#tmp`
- Related Terms: temporary, interim, transient

**todo**
- Definition: Requires action or attention
- Purpose: Indicates action needed
- Usage: `project-todo-20250301.md`, `#todo`
- Related Terms: action, task, pending

### U

**utilities**
- Definition: Helper applications and tools
- Purpose: Identifies utility content
- Usage: `~/System/utilities/`, `conversion-utility-v01.sh`, `#utility`
- Related Terms: tools, helpers, aids

### V

**v##**
- Definition: Version number with leading zeros
- Purpose: Indicates version
- Usage: `logo-v01.ai`, `report-v02.pdf`
- Related Terms: version, revision, iteration

**vault**
- Definition: Personal knowledge management system
- Purpose: Identifies knowledge base location
- Usage: `~/Knowledge/vault/`, `#vault`
- Related Terms: database, repository, knowledge-base

### W

**waiting**
- Definition: Pending external input
- Purpose: Indicates waiting status
- Usage: `project-waiting-feedback.md`, `#waiting`
- Related Terms: pending, on-hold, standby

**web**
- Definition: Web-based project or platform
- Purpose: Identifies web-related content
- Usage: `~/Projects/dev/web-application/`, `website-mockup-v01.sketch`, `#web`
- Related Terms: website, online, internet

**wiki**
- Definition: Interconnected knowledge repository
- Purpose: Identifies wiki content
- Usage: `~/Knowledge/wiki/`, `project-wiki-v01.md`, `#wiki`
- Related Terms: knowledge-base, documentation, reference

### Y

**YYYYMMDD**
- Definition: Date in ISO 8601 format
- Purpose: Indicates date in standardised format
- Usage: `meeting-notes-20250301.md`, `invoice-20250315.pdf`
- Related Terms: date, ISO-date, calendar

## 6. Domain-Specific Extensions

### 6.1 Design-Specific Terminology

These terms apply specifically to design workflows and file types:

#### Design Disciplines

- **branding**: Brand identity design (logos, style guides, brand elements)
- **ui**: User interface design (screens, components, interfaces)
- **ux**: User experience design (flows, wireframes, journey maps)
- **print**: Print design (documents, marketing materials, publications)
- **packaging**: Physical packaging design (boxes, labels, containers)
- **illustration**: Custom illustrative work (drawings, diagrams, artwork)
- **photography**: Photo-based content (product photos, portraits, scenes)
- **motion**: Animation and motion design (transitions, video, interaction)

#### Design States

- **wireframe**: Low-fidelity structural representation
- **concept**: Early exploratory design ideas
- **comp**: Comprehensive layout for presentation
- **mockup**: Realistic representation of final design
- **exploration**: Multiple design directions for comparison
- **iteration**: Progressive design refinements
- **production**: Implementation-ready design assets
- **styleguide**: Design standards documentation

#### Design Assets

- **logo**: Brand identity mark
- **icon**: Symbolic interface element
- **banner**: Promotional display element
- **hero**: Primary visual focal point
- **thumbnail**: Small preview image
- **sprite**: Collection of interface elements
- **texture**: Surface pattern or material
- **typography**: Font-focused design element

### 6.2 Development-Specific Terminology

These terms apply specifically to development workflows and file types:

#### Development Types

- **frontend**: User-facing interface code
- **backend**: Server-side processing code
- **fullstack**: Combined frontend and backend systems
- **mobile**: Mobile application development
- **web**: Web application development
- **desktop**: Desktop application development
- **embedded**: Hardware-integrated code
- **api**: Application programming interface

#### Development Components

- **component**: Modular code unit
- **module**: Functional code section
- **library**: Collection of reusable code
- **framework**: Development foundation
- **service**: Functional processing unit
- **controller**: Control flow component
- **model**: Data structure definition
- **view**: Presentation component
- **utility**: Helper functions or tools
- **test**: Testing code and frameworks

#### Development States

- **poc**: Proof of concept
- **mvp**: Minimum viable product
- **alpha**: Early testing version
- **beta**: Pre-release testing version
- **release**: Production-ready version
- **hotfix**: Urgent correction update
- **stable**: Reliable production version
- **deprecated**: Superseded but maintained

### 6.3 Content-Specific Terminology

These terms apply specifically to content creation and management:

#### Content Types

- **article**: Informational written piece
- **blog**: Web-based publication entry
- **post**: Social media content unit
- **newsletter**: Regular email publication
- **case-study**: Project analysis document
- **whitepaper**: Authoritative report
- **ebook**: Digital book publication
- **video**: Moving image content
- **podcast**: Audio content episode
- **transcript**: Text version of spoken content

#### Content States

- **outline**: Initial content structure
- **rough**: Early draft with main points
- **draft**: Work-in-progress content
- **edited**: Revised and corrected content
- **proofed**: Error-checked content
- **approved**: Client-accepted content
- **scheduled**: Time-planned content
- **published**: Publicly available content
- **archived**: Removed from active use

#### Content Components

- **headline**: Primary title text
- **subhead**: Secondary title text
- **body**: Main content text
- **caption**: Image description text
- **callout**: Highlighted text element
- **quote**: Attributed statement
- **sidebar**: Supplementary content
- **footnote**: Reference annotation
- **citation**: Source reference
- **metadata**: Content description data

## 7. Integration with Other FOMO Documents

This controlled vocabulary document works in conjunction with other FOMO project documents to form a unified system:

- **Naming Standards** (`fomo-naming-STANDARDS-v02.md`): This vocabulary provides the specific terms to use within the naming patterns established in the standards document.
- **Directory Structure** (`fomo-directory-structure-GUIDELINES-v03.md`): The terms in this vocabulary align with and support the organisation principles and folder hierarchy defined in the directory structure.
- **Project Charter** (`fomo-project-charter.md`): This vocabulary upholds the vision and principles articulated in the charter, particularly regarding clarity, consistency, and balanced implementation.
- **Implementation Plan**: The terms support the phased rollout approach, enabling incremental adoption across new files, active projects, and historical content.
- **Tag Management**: This vocabulary supersedes the sample tag vocabulary in previous guidelines, providing an authoritative source for tagging terminology.

---

_Version History:_

- v01 - 2025-03-24: Initial controlled vocabulary document created