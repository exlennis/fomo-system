# FOMO: Tag Management Guidelines v01

## 1. Introduction and Purpose

This document establishes best practices for managing tags across applications as part of the File Organisation, Management & Optimisation (FOMO) project. It provides a framework for creating and maintaining a consistent tagging system that works seamlessly across different platforms and integrates with the broader FOMO organisational structure.

Tags serve as a complementary organisational layer to the directory structure, offering flexible, cross-platform categorisation that enhances findability. While folders organise files based on a single hierarchical path, tags allow items to exist in multiple conceptual categories simultaneously.

## 2. Core Principles

### 2.1 Foundation: Establish a Controlled Tag Vocabulary

**Principle**: Define a limited set of core tags that serve as the foundation of your system. These should be broad, reusable categories that work across all applications. Use the same terminology, spelling, and case format consistently everywhere.

**Example**: Create a controlled vocabulary of 10-15 core tags such as `work`, `personal`, `finance`, `health`, `reference`, and `project`. Apply `finance` consistently rather than alternating between `finance`, `financial`, and `money`.

**Why It Matters**: A controlled vocabulary prevents tag proliferation and establishes consistent patterns that your brain can recognise across different contexts. This aligns with the FOMO Naming Standards principle of clarity and consistency.

**FOMO Integration**: This approach complements the "Directory Structure Guidelines" by providing cross-cutting organisation beyond the folder hierarchy. Similar to how Level 2+ folders use lowercase kebab-case in the directory structure, tags should follow consistent formatting.

### 2.2 Implementation: Use Tag Combinations Instead of Creating New Tags

**Principle**: Rather than creating highly specific tags for every situation, combine existing tags to create powerful filtering options. This keeps your tag list manageable while still allowing for detailed organisation.

**Example**: For a work invoice that needs payment, use `work` + `finance` + `action` rather than creating a new `work-invoice` tag. For a client project document, use `client-acme` + `project` rather than creating a separate `acme-project` tag.

**Why It Matters**: Each new tag adds mental overhead to your system. Combinations reduce the total number of tags to remember while maintaining organisational flexibility. This approach mirrors the "layered naming approach" from the FOMO Naming Standards.

**Technical Implementation**: 
- In Apple Notes: Apply multiple tags from the tag selector
- In Gmail: Apply multiple labels via filters or manually
- In Obsidian: Use space-separated tags like `#work #finance #action`

### 2.3 Context: Apply Tags Based on Purpose and Workflow Stage

**Principle**: Tag items based on their context, role in your workflow, and how you'll likely need to find them later. Consider using status tags to indicate progress or action requirements.

**Example**: 
- For an email about an upcoming project: `work` + `project` + `planning`
- For that same project after it's underway: `work` + `project` + `active`
- For project resources you're keeping for reference: `work` + `project` + `reference`

**Why It Matters**: Contextual tagging enables you to filter information based on what you're doing right now, not just what something is about. This creates views that match your mental state and current needs.

**Workflow Integration**: This approach pairs well with the "Workflow and Process Analysis" FOMO document, tracking items as they move through different stages from creation to archiving.

### 2.4 Technical: Leverage Application-Specific Features

**Principle**: Each application has unique organisational capabilities beyond basic tagging. Use these features alongside your core tags to enhance organisation without creating application-specific tags.

**Examples**:

**Apple Mail/Gmail**:
- Use smart mailboxes/filters alongside tags to automatically sort emails
- Example: Create a smart mailbox for all items tagged `work` + `action` with a due date this week
- Benefit: Reduces the need for ultra-specific tags like `work-this-week`

**Apple Notes**:
- Use folders for broad organisation and tags for cross-cutting concerns
- Example: Keep a "Recipes" folder but tag recipes with `quick`, `vegetarian`, or `dinner`
- Benefit: Combines hierarchical and tag-based organisation for maximum flexibility

**Obsidian**:
- Use YAML frontmatter to add structured metadata beyond tags
- Example: Instead of a `priority-high` tag, use frontmatter: `priority: high`
- Benefit: Reserves tags for categories while using frontmatter for properties

**Reminders**:
- Combine tags with priority flags, dates, and Smart Lists
- Example: Instead of a `urgent` tag, apply the high-priority flag to items tagged `work` + `action`
- Benefit: Uses the built-in priority system rather than creating redundant tags

**Why It Matters**: This approach leverages each application's strengths while maintaining a consistent core vocabulary, giving you the best of both worlds: specialised tools and unified organisation.

### 2.5 Evolution: Regularly Review and Refine Your Tag System

**Principle**: Schedule periodic tag reviews (every 3-6 months) to assess usage patterns, remove unused tags, and consolidate similar ones. Adapt your system as your work and needs change.

**Example**: During a quarterly review, you might notice you've created both `client` and `clients` tags. Standardise on one, update all affected items, and document the decision in your maintenance log.

**Why It Matters**: Tag systems tend to grow organically and need regular pruning to remain effective. This mirrors the "Maintenance Strategy" section of the FOMO Project Charter.

**Implementation Guide**:
1. Export or list all tags from each application
2. Identify rarely used or redundant tags
3. Consolidate similar tags
4. Update your controlled vocabulary document
5. Record changes in the FOMO Maintenance Log

## 3. Cross-Platform Implementation

### 3.1 Handling Different Tagging Mechanisms

Different applications implement tagging in various ways. Here's how to maintain consistency across major platforms:

**Flat vs. Hierarchical Tags**:
- **Flat Systems** (Apple Notes, Reminders): Use tag combinations as described in Principle 2.2
- **Hierarchical Systems** (Obsidian, some email clients): Consider whether to use hierarchical tags (e.g., `work/project/planning`) or stick with combinations of flat tags for consistency

**Format Considerations**:
- **Prefix**: Some systems use `#` (Obsidian), others don't (Apple Notes)
- **Spacing**: Some allow spaces in tags, others don't
- **Recommendation**: Use kebab-case (`client-meeting`) for maximum compatibility across systems

**Automation Opportunities**:
- Create Shortcuts automations to apply consistent tags across Apple applications
- Use email filters to automatically apply tags to incoming messages
- Configure template systems to include appropriate default tags

### 3.2 Cross-Application Consistency

**Principle**: The true power of tagging emerges when you use consistent tags across all your applications, creating a unified system that transcends individual tools.

**Example**: Using the same tags (`work` + `project` + `client-acme`) across email, notes, files, and task managers allows you to quickly gather all resources related to the Acme project regardless of where they're stored.

**Implementation Strategy**:
1. Start with core applications you use daily (email, notes, tasks)
2. Expand to include file management and knowledge systems
3. Document your tag vocabulary in a central reference
4. Create shortcuts or templates to easily apply common tag combinations

**Why It Matters**: A unified tagging approach eliminates the need to remember different organisational systems for different tools, reducing cognitive load and increasing productivity.

## 4. Sample Tag Vocabulary

### 4.1 Context Categories
- `personal`: Personal items, non-work related
- `work`: Work-related items
- `client-[name]`: Client-specific items (e.g., `client-acme`)
- `project-[name]`: Project-specific items (e.g., `project-website`)

### 4.2 Content Types
- `document`: Text-based documents
- `image`: Visual content
- `audio`: Sound recordings
- `video`: Video content
- `code`: Programming or scripting content

### 4.3 Status Indicators
- `active`: Currently being worked on
- `pending`: Awaiting action from others
- `completed`: Finished items
- `archived`: Items kept for reference
- `action`: Requires action from you

### 4.4 Topic Areas
- `finance`: Financial matters
- `health`: Health-related items
- `tech`: Technology topics
- `creative`: Design, art, or creative work
- `learning`: Educational content

## 5. Integration with FOMO Framework

This Tag Management document works in conjunction with other FOMO project documents:

- **Naming-Standards-v02.md**: Follows the same principles of clarity, consistency, and kebab-case formatting
- **Directory-Structure-v01.md**: Provides a complementary organisation layer to the folder hierarchy
- **Special-Cases-v01.md**: Addresses exceptions and domain-specific tagging requirements
- **Maintenance-Log-v01.md**: Records tag system changes and refinements over time

## 6. Success Metrics

The effectiveness of this tagging system will be measured by:

- **Retrieval Speed**: Reduction in time to locate information across applications
- **Tag Count**: Maintaining a controlled, manageable number of total tags
- **Consistency**: Percentage of items following the tagging conventions
- **Cross-Platform Usage**: Effective use of the same tags across different applications

---

_Version History:_
- v01 - 2025-03-15: Initial tag management best practices document created
