# FOMO Maintenance Log v01

This record is designed for documenting system changes, assessing performance, and planning future improvements in a single, streamlined log. Update this log regularly (e.g., weekly, monthly) to track progress and maintain an up-to-date record of your system. 

A simple record of what I tried, what worked, what broke, and what I learned along the way.

### Why Keep This Log
This is my personal breadcrumb trail so I can:
- Remember how I fixed that weird file naming issue 6 months ago
- Avoid repeating mistakes I've already made
- Track which parts of my system are actually making life easier
- Remember the "why" behind my decisions when I revisit this later

### How To Use
- **Keep it casual**: Just jot down notes when something interesting happens
- **Delegate when possible**: Let Claude or other AI assistants update it
- **Newest stuff first**: Latest entries at the top so they're easy to find
- **Focus on the useful bits**: Only record what future-me would want to know
- Formatting:
    - Use Markdown syntax for formatting.
	- Use hyphens (-) for bulleted lists.
	- Indent nested bullet points with four spaces.
	- Date format: YYYY-MM-DD
- Language: Use Australian English spelling.
- Sections: Complete each section with relevant information. Use the provided examples as a guide.
- Log Entry Title: Use a descriptive title for each log entry to quickly identify the focus of the update (e.g., "System Update & Performance Review," "Troubleshooting [Specific Issue]," "Planning Next Steps").

## Template: Maintenance Log Entry

**Template 1**

    ```markdown
    ---
    ## YYYY-MM-DD: Log Entry Title
    
    ### System Changes
    
    - **Automation Setup:** Implemented new automation processes to enhance efficiency.
    - **Organisation Efforts:** Optimised organisational structures to improve accessibility and productivity.
    
    ### Issues Encountered
    
    - **Technical Problems:** Identified and resolved technical issues that hindered system performance.
    - **Process Inefficiencies:** Recognised and rectified areas of process inefficiencies that negatively impacted workflow.
    - **User Experience Concerns:** Addressed user experience concerns to enhance overall satisfaction.
    
    ### Solutions Implemented
    
    - **Technical Solutions:** Resolved technical challenges through effective solutions.
    - **Process Improvements:** Implemented process improvements to optimise workflows.
    - **User Experience Enhancements:** Enhanced user experience through user-centric design and support.
    
    ### Future Improvements
    
    - **Ideas for Enhancement:** Identified areas for future enhancement and potential improvements.
    - **Notes for Future Reference:** Documented key findings and insights for future reference.
    
    ---
    ## Regular Check-ins
    
    #### What's Working Well
    - Parts of the system I'm happy with
    - Time-saving tricks discovered
    - Example: *"Screenshot automation is actually saving me time"*
    
    #### Pain Points
    - Things that are still frustrating
    - Bottlenecks in my workflow
    - Example: *"Still spending too much time sorting downloads"*
    
    #### Ideas to Try
    - New approaches I want to experiment with
    - Simple improvements to implement
    - Example: *"Try using Hazel to auto-sort PDFs based on content"*
    
    #### System Tweaks Made
    - Changes to my original plan based on actual usage
    - New shortcuts or rules created
    - Example: *"Added a quick screenshot renaming shortcut to Touch Bar"*
    ```
**Template 2**

    ```
    ### YYYY-MM-DD: [Log Entry Title]
    
    1. **Overview of Changes & Activities**
        - **Summary:** Briefly describe any system changes, updates, or maintenance activities performed during this period.
        - **Improvements Implemented:** List any enhancements made to improve efficiency, organisation, or user experience.
        - _Example: Implemented new screenshot automation process; Optimised folder structure for project files._
    2. **Performance & Usability Assessment**
        - **What's Working Well:** Identify aspects of the system or workflow that are functioning effectively and contributing to productivity.
        - **Challenges & Pain Points:** Note any persistent issues, bottlenecks, or frustrations encountered during usage.
        - **User Experience Notes:** Capture any observations or feedback related to the overall user experience.
        - _Example: Screenshot automation saves time; Sorting downloads remains a bottleneck; Occasional lag when using [specific application]._
    3. **Actions Taken & Solutions Applied**
        - **Solutions Implemented:** Describe the solutions implemented to address identified challenges or pain points.
        - **System Tweaks & Adjustments:** Document any modifications made to the system configuration, settings, or workflows.
        - _Example: Created Hazel rule to auto-sort PDFs; Adjusted screenshot renaming shortcut in Touch Bar._
    4. **Future Improvements & Action Items**
        - **Ideas for Enhancement:** List potential improvements, new features, or alternative approaches to explore.
        - **Action Items:** Define specific tasks or experiments to be undertaken in the next review period.
        - **Notes for Future Reference:** Document any key findings, insights, or dependencies for future consideration.
        - _Example: Explore integration with [specific application]; Test alternative PDF management tools; Review storage capacity and archiving strategy._
    ```

************

## Log Entries

---
## 2025-04-03: Prompt Library Relocation

### What I Did Today
- Relocated prompt library from `~/Knowledge/prompts/` to `~/Resources/prompts/`
- Maintained the same internal structure (data, docs, collections, templates, workshops)
- Updated all cross-references in documentation
- Revised automation scripts to use new paths

### Why I Made This Change
- Recognized prompts function more as reusable assets (Resources) than collected information (Knowledge)
- Improved alignment with FOMO's conceptual framework separating assets from catalogues
- Enhanced workflow by grouping prompts with other creative assets

### Implementation Notes
- Created identical directory structure in new location
- Used rsync to preserve metadata during migration
- Verified all files transferred successfully with checksums
- Temporarily maintained old location with symlink to new location for transition period
- Will remove old location after 2 weeks of successful operation

### Random Thoughts
- The Resources directory is proving to be the more logical home for tools that support creation
- This change better aligns with how I actually use prompts in my workflow
- Need to consider if other Knowledge items might be better categorized as Resources

---
## 20250401: Documentation and Automation Verification

### What I Did Today
- Completed comprehensive audit of workflow analysis and automation tasks
- Updated project documentation to reflect completed workflow analysis
- Verified implementation of automation scripts in both project and offsite locations
- Consolidated project status documentation across all major documents
- Renamed project checklist to "FOMO Project Starter & Status" to better reflect purpose
- Updated version histories across all documents for consistency

### What Broke
- Discovered inconsistencies between documented status and actual implementation progress
- Found missing documentation of offsite locations' relationship to main project
- Identified incomplete tracking of completed automation scripts
- Encountered formatting inconsistencies in version history sections

### How I Fixed It
- Performed thorough audit of ~/System/scripts/ directory to identify all completed tools
- Updated fomo-project-starter-and-status.md with accurate completion status
- Created proper cross-references between project and offsite locations
- Standardised version history format across all project documents
- Ensured proper attribution of automation tools to their respective locations
- Verified script implementations match documented workflows

### Random Thoughts
- The project has made significantly more progress than was reflected in documentation
- Offsite locations (~/Knowledge/docs/ and ~/System/scripts/) are proving valuable for system-wide resource sharing
- Documentation and implementation are now properly synchronised
- The renaming of the project checklist document provides better clarity of purpose
- Australian English spelling conventions are being consistently maintained across documentation

---
## 2025-03-29: Knowledge Organisation Update

### What I Did Today
- Finalised the location and structure for my prompt library
- Clarified the standards for guidelines and documentation naming
- Created a dedicated structure for AI prompt assets

### What Broke
- Previous approach with prompts in `~/Knowledge/docs/prompt-library/` didn't provide enough separation for this growing resource
- Found potential sync conflicts between GitHub version control and cloud storage when storing prompts in symlinked directories

### How I Fixed It
- Established `~/Knowledge/prompts/` as a dedicated top-level directory within the Knowledge area
- Created a structured subdirectory system for the prompt library:
  ```
  ~/Knowledge/prompts/ (renamed from prompt-library)
  ├── data/           # Supporting data for prompts
  ├── docs/           # Documentation about prompts
  ├── collections/    # Organised sets of prompts (renamed from prompts)
  ├── templates/      # Reusable prompt patterns
  └── workshops/      # Prompts under active development/testing
  ```
- Confirmed guidelines and standards documents belong in `~/Knowledge/docs/` following established naming patterns
- Positioned prompt library outside symlinked cloud directories to facilitate direct GitHub integration without sync conflicts

### Random Thoughts
- Prompt libraries are emerging as a unique type of knowledge asset that blur the line between reference material and creative development
- The decision to give prompts dedicated space recognizes their growing importance in my workflow
- Keeping standards documents in `~/Knowledge/docs/` with the established naming convention (`[topic]-[document-type]-[optional-modifier].md`) maintains consistency
- The ALL CAPS naming convention for document types (GUIDELINES, STANDARDS) provides excellent visual scanning in directory listings
- As AI plays a larger role in my workflow, the prompt library will likely become as important as design assets or code libraries

---
### 2025-03-28: Fixed Symlink Establishment Issue

#### What I Did Today
- Updated section 7.3 in the directory structure guidelines (v03)
- Added proper verification steps before creating symlinks
- Created a script to automatically backup existing directories before symlinking
- Added a clear warning note about symlink behaviour with existing directories

#### What Broke
- Discovered that symlinks were being created *inside* existing directories instead of replacing them
- This caused unexpected nested symlinks that broke the directory structure
- The original guidelines didn't account for pre-existing directories like ~/Downloads

#### How I Fixed It
- Added a loop to check for and backup existing directories before creating symlinks
- Created a more informative warning about symlink behaviour
- Structured the implementation into clear, separate steps

#### Random Thoughts
- This is a common stumbling point when implementing symlink-based structures
- The updated guidelines make the system more robust for first-time setup
- Should consider adding this kind of verification to all filesystem operations

---
### 2025-03-03: First Day Testing

#### What I Did Today
- Set up a test folder with the new kebab-case naming
- Created my first Hazel rule for screenshots
- Tried renaming about 20 random files to see how it feels

#### What Broke
- The screenshot Hazel rule choked on emoji in filenames
- Found it awkward to remember the exact order of date-project-version

#### How I Fixed It
- Added a step in Hazel to strip emojis before processing
- Made a cheat sheet for naming patterns and stuck it on my desktop

#### Random Thoughts
- The kebab-case actually looks nicer than I expected
- Automation feels worth it for screenshots since I take so many
- Still not sure about the right approach for client files - need to think about it

************

---

## Notes for AI Assistants

You can help maintain this log after we've worked on the FOMO system. Just add new entries at the top following the template. Keep it casual but useful - imagine you're leaving notes for me to find later when I inevitably forget how I solved a problem.

Some examples of when to update this log:
- After we've set up a new automation
- When we discover and fix a weird edge case
- If we change our approach to something
- When I mention something is working really well or poorly

Sample prompt I might use: "Hey Claude, can you add today's screenshot automation fixes to the maintenance log? Especially that trick we figured out for handling spaces in filenames."

---

*Version History:*
- v01 - 20250303: Initial log structure created
- v02 - 20250401: Added documentation update and automation verification entry
