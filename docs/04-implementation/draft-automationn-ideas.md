# FOMO Automation Over: Script, Rules & Workflows Draft (for reference only)

This document lists all the automation rules and components found in the FOMO system project documentation.

## Planned Automation Components

### 1. **fomo-project-charter-v01.md**:

- Project Approach Section
     - Line 55: Hazel Rule: Automation-First Mindset - Prioritise automated solutions using Hazel, Shortcuts, Python, and n8n
     - Line 56: Integration Rule: Human-Agent Collaboration - Leverage Claude's capabilities alongside human expertise
- Project Organization Section
     - Line 69: Implementation Rule: Implementation-and-Automation - Develops scripts, Hazel rules, and technical solutions
     - Line 78: Documentation Rule: FOMO-Automation-Scripts-v01.md - Technical solutions for file management
- Project Scope Section
     - Line 97: Hazel Rule: Hazel rule sets for automated file organisation
     - Line 98: Apple Shortcuts Rule: Apple Shortcuts for streamlined processing
     - Line 99: Python Script Rule: Python scripts for specialised operations
     - Line 100: n8n Rule: n8n workflows for integrated processes
     - Line 104: Automation Rule: Automated file naming and processing
- Success Criteria Section
     - Line 120: Performance Rule: Automation Coverage - 80% of routine tasks

### 2. **fomo-project-setup-plan-v01.md**:

- Guiding Principles Section
    - Line 45: Automation Rule: Prioritise Automation - Automate processes wherever possible using tools like Hazel, Shortcuts, Python scripts, and n8n workflows
- Roles and Responsibilities Section
    - Line 71-73: Implementation Rule: Implementation-and-Automation - Focuses on practical scripts and workflows, Contains automation rules for Hazel, Shortcuts, etc.
- Document Framework Section
    - Line 110-115: Documentation Rule: Automation-Scripts-v01.md - Collection of scripts for batch renaming, Hazel rules for automatic organisation, Apple Shortcuts for common file handling tasks, Python scripts for specialised operations
- Automation Approach Section
    - Line 226-231: Hazel Rule: Hazel Configuration - Create rule sets for different folders, Define pattern matching for file types, Establish naming transformations, apply naming conventions to screenshots, Set up sorting rules, Move files to appropriate directories based on type
    - Line 232-237: Apple Shortcuts Rule: Apple Shortcuts - Quick renaming of selected files, Capture and process screenshots, Standardise naming on save dialogs, Build file processing workflows
    - Line 238-242: Script Rule: Scripts (Python, AppleScript and other) - Batch rename based on conventions, Analyse compliance with standards, Generate reports on system organisation
    - Line 243-247: n8n Rule: n8n Workflows - Automate file processing for cloud services, Monitor and organise shared files, Integrate with other services
    - Line 248-254: Prioritization Rule: Automation Priorities - Screenshots and Downloads folder, High-volume file creation processes, Document save templates, Batch processing for existing files, Monitoring and reporting
- Performance Metrics Section
    - Line 329-332: Performance Rule: Automation Coverage - Automate 80% of routine file management tasks

### 3. **fomo-claude-system-instructions-v02.md**:

- Learning Objectives Section
    - Line 210-214: Skill Development Rule: Automation Skill Development - Build expertise in Hazel rule creation, Develop Apple Shortcuts proficiency, Enhance Python scripting capabilities, Explore n8n workflow potential
- System Updates Section
    - Line 188-191: Maintenance Rule: System Updates - Process for updating automation rules, Procedure for revising standards, Method for implementing new features, Path for resolving issues

### 4. **reserach-file-automation-system-grok.md**:

- Hazel Automation Section
    - Line 34-39: Hazel Rule: File Renaming - Standardise downloaded PDFs, rename to "YYYY-MM-DD_Document.pdf"
    - Line 41-45: Hazel Rule: File Sorting - Sort images to a Pictures folder
    - Line 47-51: Hazel Rule: Image Optimisation - Compress new images and tag with "Optimised"
    - Line 88-93: Hazel Rule: Hazel Automation for Tagging - Add tag "Document" to PDFs
    - Line 191: Hazel Rule: Apply naming conventions via Hazel renaming rules
- AppleScript Section
    - Line 56-67: AppleScript Rule: Example Script for compressing images in a folder
- Integration Section
    - Line 123-131: Integration Rule: Raycast Integration Custom Scripts - Example Script to open a Smart Folder
- AI Implementation Section
    - Line 141-150: AI Rule: AI Automation Exploration - Automatic Tagging using Apple's Vision framework, Content Analysis with HoudahSpot

### 5. **fomo-naming-standards-v01.md**:

- Implementation Guidelines Section
    - Line 213: Hazel Rule: Configure Hazel rules to automatically rename files based on naming standards
    - Line 214: Shortcuts Rule: Create Shortcuts for streamlined naming during save operations
    - Line 215: Python Script Rule: Develop Python scripts for batch processing and compliance checking
    - Line 216: n8n Rule: Set up n8n workflows for integrated file processing
- Version Control Integration Section
    - Line 220: Git Rule: Configure git hooks to validate file names before commit
- Success Measures Section
    - Line 311: Automation Success Rule: 80% of routine file naming handled automatically
- Benefits Section
    - Line 20: Automation Principle: Enable effective automation through predictable patterns

## Planned Automation Overview

| # | Hazel Rules | Apple Shortcuts | Python Scripts | AppleScript | n8n Workflows | Git Automation |
|---|-------------|-----------------|----------------|-------------|---------------|--------------|
| 1 | PDF Standardization | Quick Renaming | Batch Renaming | Image Compression | Cloud Processing | Filename Validator |
| 2 | Image Sorting | Screenshot Processor | Compliance Checker | Hazel Extender | File Monitor | |
| 3 | Image Compression | Save Dialog Helper | Organization Reporter | Custom Processor | Service Integrator | |
| 4 | Auto Tagging | File Workflow | File Analyzer | | | |
| 5 | Type-Based Filing | AI Vision Tagger | | | | |
| 6 | Pattern Matcher | | | | | |
| 7 | File Renamer | Save Template | | | | |

## Implementation Status

The FOMO system project is currently in its planning phase. While detailed documentation exists outlining planned automation components, implementation scripts have not yet been developed. The scripts directory exists but does not currently contain complete automation implementation files.

## Learning Objectives

Through implementing these automation components, the project aims to:

- Build expertise in Hazel rule creation
- Develop Apple Shortcuts proficiency
- Enhance Python scripting capabilities
- Explore n8n workflow potential
- Integrate with version control systems through git hooks

## Resources

https://github.com/matthewrenze/rename-images
https://github.com/jdmonaco/pdf-title-rename
https://github.com/ronakg/smart-image-renamer
https://github.com/chrissimpkins/fontname.py


*****************************************

## Automation Ideas Parking lot

- file extension consistency, change old standards to new ones, e.g. .markdown to .md, .jpeg vs .jpg???
- an automation shortcut to check for inconsistent in tag casing and suggest fixes e.g. work vs working vs Work
- an automation shortcut to check for inconsistent in file naming and suggest fixes . e.g. _ vs -
- Auoamte app update workflow > Latest installation then check macudpater and app store ? brew instlls?
- auto cover files: with a dropzone setup-
- auto Convert `.doc` or `.docx` files to `.md`
- Saved link to Reader app via #tools/Shortcuts
- save links to bookmarking #tools `Anybox`  > tagged with `feed` > added to RSS reader app like `Reeder`  
- Automatically #tools/Obsidian headings to `Title Case `


**Apple Notes**:
- Tag new notes, tag notes while transition? quickly apply tags when moving notes?
- Check for inconsistent tag casing and suggest fixes?
- Retrieve all notes and extract tags.
- Check for variations (e.g., #Work, #work, #WORK). Suggest a unified format (e.g., #work).
- Provide a list of notes needing updates so you can manually confirm before applying changes.

AI-powered content analysis workflow:
1. Scan note content and extract key topics, themes, and keywords.
2. Recommend connections between notes based on shared concepts.
3. Identify redundant or overlapping notes for better organisation.

*****************************************

### auto tag shortcut 

Apple’s Shortcuts app has received significant updates in iOS 13, and the latest version of Drafts is ready for those updates with powerful shortcuts actions that allow you to search and modify content in Drafts from Shortcuts. Combine these new powers with the Shortcuts “Automations” feature, and you can schedule shortcuts to run automatically in the background based on a variety of triggers. This tip provides an example workflow to use Shortcuts to route drafts from your Drafts inbox to Reminders based on tags assigned in Drafts - automatically archiving the drafts once they have been created in Reminders.

Consider this example a starting point. The same principle could be applied to route drafts to other locations (files, a task manager, etc.). It also allows you do things like create a draft on the watch, assign it a tag, and later have it automatically processed by the Shortcuts automation on your iPhone.

By setting up workflows like this example, you can freely capture text to Drafts - from the Watch, the Share extension, or just in the app - and just assign tags to have those drafts automatically processed and archived without any additional action on your part.

#### Drafts Tagged “Reminders” to Reminders Shortcut

[![shortcuts-example](https://forums.getdrafts.com/uploads/default/optimized/2X/f/f89025c71c1aa18a5d7cef98f8c0d181970d887d_2_690x386.png)

](https://forums.getdrafts.com/uploads/default/original/2X/f/f89025c71c1aa18a5d7cef98f8c0d181970d887d.png "shortcuts-example")

To start, install the example shortcut from the link below (NOTE: _To install third party shortcuts in the Shortcuts app, you will have to enable “Allow untrusted shortcuts” in iOS Settings > Shortcuts_):

**Install Example Shortcut**: [Drafts Tagged “Reminders” to Reminders 235](https://www.icloud.com/shortcuts/66999ddd92b447e0b30eb363be6a9805)

#### Modifying the Shortcut

The example shortcut consists of several actions (see attached). These actions might need to be modified to suit your needs. Let’s review what each does and what modifications you might want to make…

[![IMG_0523](https://forums.getdrafts.com/uploads/default/optimized/2X/1/19e2937ebf667bc0bc91aba8a9cb4718b0820849_2_315x500.jpeg)

](https://forums.getdrafts.com/uploads/default/original/2X/1/19e2937ebf667bc0bc91aba8a9cb4718b0820849.jpeg "IMG_0523")

- **Search Drafts**: This action searches for any drafts in your drafts list which match the specified criteria. In this example, the action has been configured to only search the “Inbox” for drafts with the tag “reminder”. If you wish to use a different tag to identify drafts for use in this shortcut, you can edit the tag value.
- **Repeat with each item in `Drafts`**: The search returns a list of drafts matching the search. Using the repeat action, you can loop over each of those drafts performing a set of actions on each.
    - **Add `Title` to `Reminders`**: This is a shortcut “Add to Reminders” action configured to create a reminder in the Reminders app, in the list “Reminders”. The reminder with use the `Title`property (first line) of the draft, and include a link to the draft in Drafts, and the full content of the draft in the notes. If you want to route to a different list in Reminders, tap on the “Reminders” entry to select from your available Reminder lists. This action could also be replaced by another shortcut action if you wanted to route to a different app or file.
    - **File `Repeat Item` in `Archive`:** This `File Draft`action moves the draft out of the inbox to the archive in Drafts. This item could be modified to assign an additional tag, or even moe the draft to the trash.
- **End Repeat**: Complete the loop

#### Testing The Shortcut

To test operation fo the shortcut (assuming you have made no mofications above), do the following:

- Open Drafts
- Create a one or more new drafts, assign them the tag “reminder”.
- Go to Shortcuts and run the “Drafts Tagged ‘Reminder’ to Reminders” action.
- Go to the Reminders app. Your “Reminder” list should have new tasks for each of the draft you created in the first step.
- Go to Drafts. The draft you created should now be moved to the Archive.

#### Automating the Shortcut

[![IMG_2991](https://forums.getdrafts.com/uploads/default/optimized/2X/7/735d1c96f1ad730ec82f8fb18b2eaf155ccf946c_2_240x250.jpeg)

](https://forums.getdrafts.com/uploads/default/original/2X/7/735d1c96f1ad730ec82f8fb18b2eaf155ccf946c.jpeg "IMG_2991")

Now you have the shortcut installed, and possibly tweaked to route your tagged drafts in a particular manner. You can run this shortcut manually as needed anytime to do your routing, but you could also use the new [Shortcuts Automation 72](https://www.macstories.net/news/the-full-list-of-automation-triggers-in-shortcuts-for-ios-13/) feature to have that routing done automatically based on a trigger. There are many triggers available, what makes sense for your needs may vary, but you might make a timed trigger that sweeps your inbox and converts those reminders once a day at a certain time, for example. To setup automation, just open the Shortcuts app, and “Create Personal Automation” on the “Automation” tab.

#### Conclusion

This example exactly as configured may not suit your needs, but hopefully it will give you some ideas of how you can use the powerful new Shortcuts integration features to process all those snippets you grab in Drafts!


  
<!--## Convert `.doc` or `.docx` files to `.md`

Below are three methods using **Pandoc**, Python, or AppleScript to automate this process.

**Method 1: Pandoc (Best for Batch Conversion)**

> Pandoc is the most powerful tool for document conversion.

1. **Install Pandoc**, 
    ```sh
    brew install pandoc
    ```
2. **Convert a Single File**
    ```sh
    pandoc input.docx -t markdown -o output.md
    ```

3. **Batch Convert All `.docx` in a Folder**
    ```sh
    for file in *.docx; do pandoc "$file" -t markdown -o "${file%.docx}.md"; done
    ```

4. **Automate with a Scheduled Script**
   Create a cron job (Linux/macOS) or a scheduled task (Windows) to run the script automatically.

**Method 2: Python + Pandoc (For More Control)**

> Use Python with Pandoc to automate batch conversion.

1. Install Dependencies

    ```sh
    pip install pypandoc
    ```

2. Python Script

    ```python
    import os
    import pypandoc
    
    input_folder = "path/to/docx/files"
    output_folder = "path/to/md/output"
    
    for filename in os.listdir(input_folder):
        if filename.endswith(".docx") or filename.endswith(".doc"):
            input_path = os.path.join(input_folder, filename)
            output_path = os.path.join(output_folder, filename.rsplit(".", 1)[0] + ".md")
    
            pypandoc.convert_file(input_path, 'md', outputfile=output_path)
            print(f"Converted: {filename} → {output_path}")
    ```

3. Automate the Script: Add to `crontab -e`

    ```sh
    0 * * * * /usr/bin/python3 /path/to/script.py
    ```-->

---
