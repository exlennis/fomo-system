# FOMO Project System Instructions

## Project Setup Instructions

### Claude Project Structure

1. **Create a New Project**
	- Name: “FOMO System”
	- Description: “The File Organisation, Management & Optimisation  (FOMO) project aims to create a practical file management system with clear naming conventions and directory structures suitable for the personal needs. This project builds upon Claude’s projects, artefacts, and analytics tools to establish an elegant framework that is clear and concise, structured but not limiting, easy to implementation, and can be consistently applied and automated by both human and agents.”

2. **Set Up Core Conversations**
	- **Main-System-Planning**: Central hub for coordination and final documents
	- **Research-and-Standards**: For convention documentation and examples
	- **Workflow-and-Process-Analysis**: Identifies bottlenecks and pain points
	- **Implementation-and-Automation**: For scripts, workflows, and technical solutions
	- **Special-Cases-and-Exceptions**: For handling edge cases and unique file types

### Artifacts Creation Guidelines

1. **Artifact Naming Standards**
	- Use kebab-case for all artifact titles
	- Follow pattern: `[Document-Type]-[Description]-v[##]`
	- Example: `Guide-Naming-Standards-v01`

2. **Standard Sections for All Documents**
	- Title and version number
	- Brief introduction and purpose statement
	- Table of contents for longer documents
	- Main content with clear headings
	- Examples/illustrations
	- Version history

3. **Formatting Standards**
	- Use GitHub Flavoured Markdown (GFM) for all documentation
	- Organise with hierarchical headings (# for main, ## for sections)
	- Use code blocks for examples: ```example-file-name.ext```
	- Create tables for comparisons and structured information
	- Use bullet points to list related items without a specific order
	- Use numbered lists for sequential instructions
	- Include diagrams where helpful (Mermaid if complex relationships)

4. **Content Guidelines**
	- Be concise but comprehensive
	- Use examples liberally
	- Include rationales for decisions
	- Anticipate questions and edge cases
	- Focus on practical application

### Version Control and Documentation

To maintain clarity and track changes, all project artifacts follow this version control and documentation system:

1. **Version Numbering**: Use `v##` format (e.g., `v01`, `v02`) appended to artifact names.
	- Start at v01 and increment for each significant revision.

2. **Version History**: Include a `Version History` section at the end of each artifact with:
	- Version number
	- Date (YYYY-MM-DD)
	- Concise description of changes
	- Example: `- v01 - 2025-02-26: Initial plan created`

3. **Change Types and Handling:**
	- *Minor Updates:* For small edits (typos, formatting, clarity improvements)
		- Update artifact directly without changing version number
		- Record in `ChangeLog` with date and brief description
	- *Significant Changes:* Require new version number (increment v##)
		- Content additions or removals
		- Structural reorganisation
		- Process modifications
		- Standard/requirement updates
		- Response to formal review feedback
		- Changes affecting other artifacts or workflows
		- Record in "Version History" section with date and description

4. **Version Decision Guidance:**
	- Create new versions when changes impact how the document is used or understood
	- Multiple minor updates may collectively justify a new version
	- When in doubt, prioritise clarity, check with project manager before updating version numbers

5. **Cross-Referencing:**
	- Use format: `Document Name v##` or `Document Name - Current Version`
	- Link to specific sections where possible using heading anchors
	- Update references when target artifacts receive version changes

6. **Central Changelog:** Maintain a `Changelog` section in the `Project Management Checklist` artifact that:
	- Lists all updates chronologically (newest first)
	- Includes date, artifact name and version
	- Provides brief change summary
	- Distinguishes between major versions and minor updates
	- Links to relevant artifacts

### Using Claude's Analytics Tool
	
1. **File Analysis Scripts**
	- Use the Analytics Tool to create JavaScript for analysing file structures
	- Develop code to validate naming conventions
	- Create path manipulation utilities
	- Test automation scripts before implementing
	
2. **Data Visualisation**
	- Generate visual representations of directory structures
	- Create frequency charts of file types
	- Analyse compliance with naming conventions over time
	- Visualise before/after implementation comparisons
	
3. **Script Development Process**
	- Create initial script in Analytics Tool
	- Test with sample data
	- Debug and refine
	- Document with inline comments
	- Export for implementation

---

## Implementation Guidelines

### Design Asset Management

1. **Asset Organisation**
	- Categorise assets by type (images, fonts, templates)
	- Tag assets with relevant metadata
	- Establish version control for design files
	- Create project-specific asset collections
	
2. **Cloud Integration**
	- Configure libraries to align with file system
	- Establish naming consistency across applications
	- Manage linked assets appropriately
	- Structure project files for efficient access
	
3. **Font Management**
	- Organise fonts by family and style
	- Document licensing information
	- Create project-specific font collections
	- Implement activation/deactivation workflow

### Industry Specific Considerations

1. **Sensitive Content Handling**
	- Develop protocols for confidential information
	- Create secure storage areas
	- Establish clear identification for sensitive files
	- Document retention policies
	
2. **Client Materials Organisation**
	- Structure by client/family
	- Separate by project type
	- Categorise by project stage
	- Include relevant designations

3. **Compliance Documentation**
	- Organise legal documents
	- Track permissions and releases
	- Maintain audit trails
	- Archive according to regulations

---

## Testing and Evaluation

1. **Implementation Testing**
	- Verify script functionality with sample files
	- Test automation on non-critical directories first
	- Validate across different file types
	- Check compatibility with all tools and applications

2. **Usability Assessment**
	- Evaluate time required to find specific files
	- Measure cognitive load during file operations
	- Test with common workflow scenarios
	- Gather subjective feedback on the system
	
3. **Performance Monitoring**
	- Track automation success rates
	- Measure system compliance over time
	- Document time savings
	- Identify areas for refinement

## Maintenance Procedures

1. **Regular Review Process**
	- Schedule weekly quick checks
	- Conduct monthly system evaluations
	- Perform quarterly standard revisions
	- Document all changes and improvements
	
2. **System Updates**
	- Process for updating automation rules
	- Procedure for revising standards
	- Method for implementing new features
	- Path for resolving issues
	
3. **Knowledge Management**
	- Update documentation with lessons learned
	- Refine cheatsheets based on usage patterns
	- Maintain a troubleshooting guide
	- Document workarounds for limitations

---

## Learning Objectives for Project Implementation

1. **Claude Project Feature Mastery**
	- Effectively use conversation organisation
	- Master artifact creation and management
	- Leverage Analytics Tool for code development
	- Learn optimal information structuring
	
2. **Automation Skill Development**
	- Build expertise in Hazel rule creation
	- Develop Apple Shortcuts proficiency
	- Enhance Python scripting capabilities
	- Explore n8n workflow potential
	
3. **System Design Principles**
	- Practice balancing comprehensiveness with usability
	- Learn iterative improvement methodologies
	- Develop documentation best practices
	- Master technical implementation of theoretical standards

---

*Version History:*
- v01 - 2025-02-26: Initial instructions created
