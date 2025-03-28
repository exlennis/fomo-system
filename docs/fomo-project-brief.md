# FOMO Project Setup Plan

## 1. Project Overview

The File Organisation, Management & Optimisation project (code named FOMO) aims to create a practical file management system with clear naming conventions and directory structures that can be consistently applied and automated.

> Why the name FOMO? Because there's a "fear of missing out" on one special character that could cause mayhem for both humans and agents.

File naming and directory structure foundations are essential to any modern system, whether personal or enterprise-level.

This plan provides a balanced approach that respects the need for thorough standards while emphasising practical implementation. By focusing on automation from the start and implementing in phases, the system can deliver value immediately while evolving over time.

**Background**

> My plan is to use agents via terminal commands for much of the implementation, initial clean-up, ongoing maintenance and regular checks. This approach requires clear, consistent documentation to ensure the system functions correctly.

As a designer on a development journey, my file system contains a diverse range of document types requiring domain-specific considerations:

- **Design Projects**: Files are phase and revision-based (temporal), yet contain substantial visual reference materials. Final deliverables/branded assets are intended for long-term usage (not time-based). Due to client-facing nature, human readability is crucial.

- **Development Projects**: Research outlines different naming requirements for different languages. These projects are iterative in nature, with compatibility and machine readability being key considerations, often emphasising CI/CD practices.

- **Personal Files**: Screenshots, freelance invoices, personal documents and work files require varying organisation approaches.

- **Special Collections**: An extensive font library, design asset collections, Markdown notes in Obsidian values and reference materials need specific organisation strategies.

An elegant framework should be clear and concise for ease of implementation. It should be structured but not limiting, with consideration for special cases.

**Guiding Principles:**
- Prioritise clarity and consistency over complexity that suit individual usage.
- Strive for a balanced approach between standards and practical applications.
- Incorporate usage patterns and workflow observations into the standards.
- Ensure the solution is both readable by humans and processable by machines.
- Roll out the changes in phases to reduce disruptions during adoption.

## 2. Project Requirements

This project builds upon Claude’s projects, artefacts, and analytics tools to create a well-organised, maintainable system optimised for both human and agent interaction. In terms of importance, the project requires:

1. **Centralise Documentation**: Create a single reference point for the file management system project through persistent documentation.
2. **Establish Project Structure**: Set up core conversations and essential artefacts. Maintain version tracking as standards evolve.
3. **Implement in Clear Phases**: Adopt a phased approach, beginning with new files and progressively working backwards.
4. **Define Explicit Standards**: Develop standards based on thorough research and testing, including naming conventions, file structures, workflow processes, and automation rules.
5. **Interactive Testing**: Conduct iterative testing of naming patterns and rules to provide immediate feedback on proposed conventions.
6. **Prioritise Automation**: Automate processes wherever possible using tools like Hazel, Shortcuts, Python scripts, and n8n workflows.
7. **Ensure Safe Code Generation**: Prioritise safety in the development of automation scripts and tooling.
8. **Harness Claude's Capabilities**: Use this project as an opportunity to master Claude's project management, documentation, and analytical tools.
9. **Maintain Project Coherence**: Proactively summarise discussions, cross-reference documentation, and maintain structured conversations to keep the project focused and on track.

## 3. Core Conversations

Five core conversations will structure this project:
a. **Main-System-Planning**
	- Central hub for coordinating all aspects of the project
	- Contains final versions of all core documents
	- Tracks decisions and changes to standards

b. **Research-and-Standards**
	- Synthesises findings from existing research
	- Identifies gaps requiring further research
	- Documents final decisions on naming conventions
	- Houses reference materials and examples\

c. **Workflow-and-Process-Analysis**
	- Maps file creation sources and movement from generation to archiving
	- Identifies bottlenecks, manual tasks, and automation opportunities
	- Documents user journey decision points and integration handoffs
	- Evaluates feasibility and quantifies potential time savings

d. **Implementation-and-Automation**
	- Focuses on practical scripts and workflows
	- Contains automation rules for Hazel, Shortcuts, etc.
	- Tracks implementation progress and challenges

e. **Special-Cases-and-Exceptions**
	- Documents specific handling for screenshots, downloads, etc.
	- Addresses edge cases that don't fit the general rules
	- Provides guidelines for unusual file types

## 4. Essential Artifacts

This project will maintain 9 essential documents, keeping them updated and maintained as the project progresses:

1. **Project-Charter-v01.md**
	- Single-page overview of goals, principles, and scope
	- Brief summary of key decisions and standards
	- Quick reference for the project's purpose

2. **Naming-Standards-v01.md**
	- Comprehensive guide to file naming conventions
	- Officially adopts kebab-case as the standard
	- Includes examples for common file types
	- Documents date format (YYYYMMDD) and versioning (v01)
	- Lists prohibited characters and special handling rules

3. **Directory-Structure-v01.md**
	- Defines the folder hierarchy and organisation.
	- Limits nesting to a maximum of 3-4 levels.
	- Maps file types to appropriate locations.
	- Includes visual diagrams of the structure.
	- Analyses the file trail and workflow to justify and prioritise implementation decisions.

4. **Implementation-Plan-v01.md**
	- Step-by-step guide for implementing the system
	- Create simplified process diagrams for key workflows
	- Phases implementation from most to least critical areas
	- Includes timelines and milestones
	- Provides success criteria for each phase

5. **Automation-Scripts-v01.md**
	- Collection of scripts for batch renaming
	- Hazel rules for automatic organisation
	- Apple Shortcuts for common file handling tasks
	- Python scripts for specialised operations

6. **Special-Cases-v01.md**
	- Document workflow-specific edge cases and situations where standard naming might require exceptions based on workflow requirements.
	- Handle screenshots and downloads, create guidelines for project files, design assets, and other relevant files.
	- Provide solutions for challenging file types and exceptions to general rules, with justifications for each.

7. **Naming-Cheatsheet-v01.md**
	- Single-page quick reference guide
	- Essential patterns and examples
	- Common file type templates
	- Ready-to-use for daily application

8. **Maintenance-Log-v01.md**
	- Serves as a historical record of system changes
	- Documents issues encountered, solutions applied, and lessons learned. Tracks compliance and effectiveness over time
	- Retrospective and accumulative: Intended for after the implementation is complete to document the evolution of the system
	- Becomes more valuable as the system matures due to the accumulation of historical changes and lesson

9. **Project-Management-Checklist-v01.md**
	- Functions as an active tool for project management and task tracking
	- Organises tasks to be completed, monitors the current status, and lists next steps
	- Proactive: Used during the implementation phases with frequent updates. More active during the initial setup and implementation
	- Intended for immediate use by project collaborators

## 5. Implementation Timeline

### Phase 1: Foundation Setup (Week 1)
- Finalise all core documents
- Set up directory structure for a test area
- Create basic automation scripts
- Establish maintenance log structure

### Phase 2: New Files Implementation (Weeks 2-3)
- Apply conventions to all new files going forward
- Set up Hazel rules for Downloads folder
- Create Shortcuts for screenshots and common file types
- Test automation on small batches of files

### Phase 3: Active Projects (Weeks 4-6)
- Implement standards on current active projects
- Update references in documents
- Apply directory structure to working folders
- Refine automation based on real-world usage

### Phase 4: Historical Content (Ongoing)
- Gradually apply standards to archived content
- Prioritise high-value historical content
- Document exceptions for legacy systems
- Schedule regular review sessions

## 6. Key Technical Decisions

The following decisions have been finalised based on initial research. Additional refinements may be made based on workflow analysis and testing:

1. **Primary File Naming Convention**
	- **Standard:** kebab-case (hyphen-delimited)
	- Example: `project-name-document-v01.pdf`
	- Rationale: Best balance of readability, URL compatibility, and automation support

2. **Date Format**
	- **Standard:** ISO 8601 (YYYYMMDD)
	- Example: `project-meeting-notes-20250301.md`
	- Rationale: Ensures chronological sorting and international compatibility

3. **Version Numbering**
	- **Standard:** v01, v02 format with leading zeros
	- Example: `presentation-client-v03.pptx`
	- Rationale: Maintains correct sorting order in file listings

4. **Special Character Policy**
	- **Prohibited:** `!@#$%^&*()=+[]{};:'"\|,/<>?`
	- **Allowed:** hyphens, periods (for specific uses)
	- Rationale: Ensures cross-platform compatibility and URL-friendliness

5. **Specific File Type Templates** (To be refined through testing)
	a. **Documents**

	```
	[project]-[type]-[descriptor]-[YYYYMMDD]-v[##].[ext]
	```

	Example: `fomo-report-quarterly-20250301-v02.pdf`
	
	b. **Screenshots**
	
	```
	screenshot-[device]-[context]-[YYYYMMDD]-[HHMMSS].[ext]
	```
	
	Example: `screenshot-macbook-safari-20250301-143022.png`
	
	c. **Design Assets**
	
	```
	[project]-[asset-type]-[descriptor]-v[##].[ext]
	```
	
	Example: `fomo-logo-dark-v03.svg`
	
	d. **Code Files**
	
	```
	[function/purpose]-[language].[ext]
	```
	
	Example: `file-renamer.py`
   
## 7. Automation Approach

### Tools to Leverage (To be finalised through testing)

1. **Hazel Configuration**
	- Create rule sets for different folders
	- Define pattern matching for file types
	- Establish naming transformations, apply naming conventions to screenshots
	- Set up sorting rules, Move files to appropriate directories based on type

2. **Apple Shortcuts**
	- Quick renaming of selected files
	- Capture and process screenshots
	- Standardise naming on save dialogs
	- Build file processing workflows

3. **Scripts (Python, AppleScript and other)**
	- Batch rename based on conventions
	- Analyse compliance with standards
	- Generate reports on system organisation

4. **n8n Workflows**
	- Automate file processing for cloud services
	- Monitor and organise shared files
	- Integrate with other services

### Automation Priorities
1. Screenshots and Downloads folder (immediate value)
2. High-volume file creation processes (identified through workflow analysis)
3. Document save templates (prevents issues at source)
4. Batch processing for existing files (as needed)
5. Monitoring and reporting (for maintenance)

## 8. Claude Features Utilisation

Throughout this project, Claude should ensure:

1. **Master Projects Feature**
	- Organise conversations effectively by topic
	- Maintain context across different aspects of the system
	- Use project structure to track progress

2. **Leverage Artifacts**
	- Create and update documentation in structured formats
	- Use versioning to track document evolution
	- Cross-reference between related artifacts

3. **Utilise Analytics Tool**
	- Develop and test automation scripts
	- Analyse file naming patterns
	- Create visualisations of directory structures

4. **Maintain Context**
	- Keep conversation summaries updated
	- Link related discussions across conversations
	- Build a knowledge base within the project

## 9. Maintenance Strategy

- **Weekly Review:** Brief check of recently created files for compliance
- **Monthly Audit:** Sample testing of organisation system effectiveness
- **Quarterly Refinement:** Update standards based on practical experience
- **Continuous Improvement:** Document new challenges and solutions in Maintenance Log

## 10. Success Metrics

- **Searchability:** Time to locate specific files is reduced
- **Consistency:** New files follow conventions without manual intervention
- **Automation:** Majority of naming and organising happens automatically
- **Reduced Cognitive Load:** Less time spent deciding where/how to save files
- **Adaptability:** System evolves based on changing needs without complete overhaul

### Efficiency Metrics

**File Location Time:** Reduce average time to locate specific files by 50%
  - Baseline measurement: [TBD from initial workflow analysis]
  - Target: [TBD] seconds per file retrieval
  - Measurement method: Timed tests with standard file search scenarios

**File Processing Time:** Reduce time spent on manual file management by 75%
  - Baseline: [TBD] minutes per day (estimated from workflow analysis)
  - Target: [TBD] minutes per day
  - Measurement: Time tracking on file management tasks

### Quality Metrics

**Naming Compliance:** Achieve 95% compliance with naming conventions for new files
  - Measurement: Monthly random sampling of new files
  - Tracking: Compliance percentage in Maintenance Log

**Organisation Consistency:** Achieve 90% correct file placement
  - Measurement: Monthly directory structure audit
  - Tracking: Percentage of files in correct locations

### User Experience Metrics

**Cognitive Load:** Reduce decision points during file saving by 80%
  - Baseline: [TBD] decisions per file save (from workflow analysis)
  - Target: Automated placement with minimal user intervention
  - Measurement: User feedback and decision point mapping

**System Satisfaction:** Achieve 8/10 satisfaction rating with system
  - Measurement: Quarterly self-assessment questionnaire
  - Tracking: Satisfaction trends over time

### Implementation Metrics

**Automation Coverage:** Automate 80% of routine file management tasks
  - Measurement: Percentage of identified tasks with automation solutions
  - Tracking: Task automation inventory in Maintenance Log

**Adoption Rate:** Achieve 100% adoption for new files, 50% for historical content
  - Measurement: Compliance audits at phase completion
  - Tracking: Percentage of files following new system

---

*Version History:*
- v01 - 2025-02-26: Initial plan created