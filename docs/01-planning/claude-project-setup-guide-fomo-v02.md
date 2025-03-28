## Primary Project Hub

Create a central Claude project titled "FOMO System" with these components:

### **Knowledge Base Section**
- Upload the core reference documents (Project Charter, Naming Standards, etc.)
- Add relevant research articles and existing systems documentation
- Include any current file structure examples or screenshots

### **Core Conversations Structure**
Each conversation should have a clear purpose and contain specific artefacts:

**a. Main-System-Planning:**
   - Create the Project-Charter-v01.md artefact pin it at the top for easy reference
   - Use Extended Thinking (Better handles the interconnected nature of file organisation rules and workflows)
     - In the Main-System-Planning conversation, ask: "Based on the uploaded documents, please draft a Project Charter artefact for the FOMO system"
     - Review the draft and request specific modifications
     - Once finalised, it becomes your reference point for project scope and goals
     - Suggested Charter Structure:

```
# FOMO Project Charter v01

## Project Vision
[One-paragraph vision statement]

## Objectives
1. [Primary objective]
2. [Secondary objectives...]

## Scope
### In Scope
- [List of included elements]

### Out of Scope
- [List of explicitly excluded elements]

## Success Criteria
- [Measurable outcomes that define success]

## Key Principles
- [Guiding principles for the project]

## Stakeholders
- [Primary user(s)]
- [System maintainers]

## Project Approach
- [...]

## Key Deliverables
- [...]

## Timeline Overview
- [High-level implementation phases]

## Version History
- v01 - 2025-02-28: Initial charter created
```
		
   - Create Project-Checklist-v01.md as an artefact  tracking progress across all work-streams
     - Use this as central tracking document that gets updated frequently
   - Create Maintenance-Log-v01.md as an artefact in the Main-System-Planning conversation
     - Structure it with: System Changes , Issues Encountered, Solutions Implemented, Lessons Learned, etc.
     - Update it with clear date entries (newest first) after each significant implementation task
     - Review it before making system changes to avoid repeating mistakes

```
# FOMO System Maintenance Log

*This log tracks the historical record of system changes, issues encountered, solutions applied, and lessons learned.*

## 2025-02-28

### System Changes
- Added new Hazel rule for screenshot processing
- Updated naming convention for client files

### Issues Encountered
- Screenshot automation failed for files with special characters

### Solutions Implemented
- Modified regex pattern in Hazel rule to handle special characters

### Lessons Learned
- Always test automation with edge cases before full implementation

## 2025-02-27
[entries continue...]

```

   **b. Research-and-Standards**
   - Use Extended Thinking (benefits from deeper analysis)
   - Create artefacts for:
     - Naming-Standards-v01.md (primary artefact)
     - Research findings summaries
     - Alternative approaches comparison table
   - Use the analytics tool to analyse sample datasets of your files

   **c. Workflow-and-Process-Analysis**
   - Use Extended Thinking (helps with complex workflow mapping)
   - Create a Directory-Structure-v01.md artefact
   - Develop process flow diagrams using Mermaid
   - Use the analytics tool to identify patterns in your current workflows

   **d. Implementation-and-Automation**
   - Use Extended Thinking (better code generation and testing)
   - House Automation-Scripts-v01.md as a living document
   - Create code artefacts for:
     - Hazel rules (as screenshots or descriptive text)
     - Python scripts for batch operations
     - Shortcuts descriptions and logic

```
- Hazel Configuration
	- Create rule sets for different folders
	- Define pattern matching for file types
	- Establish naming transformations, apply naming conventions to screenshots
	- Set up sorting rules, Move files to appropriate directories based on type
	
- Apple Shortcuts
	- Quick renaming of selected files
	- Capture and process screenshots
	- Standardise naming on save dialogs
	- Build file processing workflows
	
- Scripts (Python, AppleScript and other)
	- Batch rename based on conventions
	- Analyse compliance with standards
	- Generate reports on system organisation
	
- n8n Workflows
	- Automate file processing for cloud services
	- Monitor and organise shared files
	- Integrate with other services
```

   - Implementation-Plan-v01.md with clear phases

   **e. Special-Cases-and-Exceptions**
   - Use Normal mode is sufficient for more straightforward documentation
   - Special-Cases-v01.md artefact
   - Exception handling decision tree diagram
   - Naming-Cheatsheet-v01.md as a quick reference

---

## GitHub Integration

- Create a GitHub repository called "FOMO-system"
- Structure with folders that mirror your core conversations:

```txt
/docs               # For all markdown documentation
/scripts            # Automation scripts
	/hazel            # Hazel rules
	/pythonsScript    # Python utilities
	/ApplShortcuts    # Apple Shortcuts descriptions
	/...
/resources          # reserach and reference materials 
/templates          # Template files for quick use
```

- Connect this repository to your Claude project
- This gives you the most flexibility for managing code files and documentation

## Implementation Approach

1. **Start with Standards Documentation**
	- Begin by finalising your naming conventions in the Research-and-Standards conversation
	- Use Claude to generate and test naming patterns against sample filenames
	- Document decisions in the Naming-Standards artefact
2. **Develop Structure Simultaneously**
	- Work on Directory-Structure-v01.md in the Workflow conversation
	- Use Mermaid diagrams to visualise folder hierarchies
	- Test the structure with sample file routing scenarios
3. **Create Implementation Tools**
	- Once standards are established, develop automation scripts
	- Use Claude to generate code artefacts for each automation tool
	- Store final versions in GitHub for version control
4. **Test and Refine**
	- Document testing results in the Main-System-Planning conversation
	- Update artefacts as needed based on findings
	- Create the Maintenance-Log to track changes
	
---

## Tips for Effective Use of Claude's Features
	
1. **artefacts Management**
	- Use descriptive IDs for all artefacts that include the document name and version
	- When updating artefacts, use the update function rather than creating duplicates
	- Download critical artefacts regularly as backup
2. **Maximising Analytics Tool**
	- Use it to analyse patterns in your existing files
	- Test naming convention rules against sample datasets
	- Validate automation logic before implementation
3. **Effective Conversation Management**
	- Start each conversation with a clear purpose statement
	- Periodically summarise progress and decisions
	- Cross-reference related discussions between conversations
	

### Project Management in Claude

1. **Centralise in Main-System-Planning**
	- Keep your Project Management Checklist and Project Charter in this conversation
	- Use this as your command centre for the entire project
2. **Regular Update Sessions**
	- Schedule specific sessions for updating the checklist
	- Example: "Let's review and update the Project Management Checklist based on today's progress"
3. **Cross-Reference System**
	- When referencing work done in other conversations, note it in the checklist
	- Example: "Update checklist to note completion of naming convention research in Research-and-Standards conversation"
4. **Version Control Application**
	- Apply your versioning system to track major changes
	- For the frequently updated checklist, add a "Last Updated" date at the bottom
	
You've raised an important point about potential confusion with document updates. Here's how updates affect artefacts in both locations and key considerations for managing this:

### Updates and Version Management

When you update the Project Charter artefact:
- The update only affects the version in the artefacts section
- The copy in the Knowledge Base remains unchanged
- This creates a version discrepancy between the two locations

This can indeed lead to confusion about which version is current and authoritative.

**Recommended Approach** to maintain clarity and version control:

1. **Primary Location Strategy**
   - Choose one location as the "source of truth" (I recommend the artefact version)
   - Always make updates to this version
   - Consider adding a note at the top of the Knowledge Base version: "This is a reference copy. See the artefact version for the most current document."

2. **Update Workflow**
   - After updating the artefact version, download it
   - Delete the outdated Knowledge Base version
   - Upload the new version to the Knowledge Base
   - This maintains alignment but requires manual synchronization

3. **Version Tracking**
   - Use clear version numbering in the filename (v01, v02)
   - Include a "Last Updated" date in the document header
   - Maintain a detailed version history section
   - These provide visual cues about which version is current

### Key Points About Knowledge Base and artefacts

1. **Search Functionality**
   - Knowledge Base items are included in project search results
   - artefacts in conversations may be harder to locate via search
   - This can make Knowledge Base versions more discoverable

2. **Conversation Context**
   - artefacts retain the conversation context in which they were created/updated
   - Knowledge Base items lack this context
   - This context can be valuable for understanding the reasoning behind changes

3. **Download and Export**
   - Both artefacts and Knowledge Base items can be downloaded
   - Consider periodic exports of key documents as backups

4. **Related Files Organization**
   - Knowledge Base allows you to organize related files together
   - This can be valuable for grouping the Project Charter with supporting materials

5. **Permanence Considerations**
   - Knowledge Base items remain even if conversations are deleted
   - This provides a level of permanence for critical documents

For your FOMO project, I recommend maintaining the Project Charter primarily as an artefact and only adding stable, "release" versions to the Knowledge Base. This balances the benefits of both locations while minimizing confusion about which version is current.
