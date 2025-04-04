# Architectural Reasoning Behind the FOMO Directory Structure

## Asset Symlinking Philosophy

### Rationale for Entire Assets Folder Symlinking

The proposal to symlink the entire assets folder rather than individual components stems from several architectural principles:
- **Structural Coherence**: Maintaining the complete assets hierarchy preserves contextual relationships between different asset types
- **Update Propagation**: Any changes to the cloud structure automatically appear in your logical view without manual intervention
- **Simplicity of Maintenance**: Managing a single high-level symlink reduces the complexity of your directory structure
- **Mental Model Alignment**: Your existing categorization within Dropbox remains intact while gaining the benefits of easier access

Rather than fragmenting your asset structure with multiple granular symlinks, this approach creates a clean "window" into your existing organization while minimizing potential sync issues.

### Font Folder Placement Considerations

The dual presentation of fonts (within assets/fonts and as a separate Resources/fonts entry) highlights a fundamental tension in directory architecture:
- **Domain-Crossing Resources**: Fonts span multiple domains (system, design, documents) unlike most other assets
- **Application Integration**: Font management tools often expect specialized locations
- **Frequency of Access**: Typography elements typically warrant more direct access than other asset types

This treatment recognizes fonts as both design assets (organizational relationship) and system-wide resources (functional relationship). However, it does introduce potential confusion in the conceptual model, which may warrant reconsideration.

## Asset Management Philosophical Approaches

### Eagle Library's Conceptual Model vs. Traditional Systems

Eagle represents a fundamentally different approach to asset management:
- **Database vs. Filesystem**: Eagle uses a database overlay atop physical files, separating organization from storage
- **Visual Primacy**: Prioritizes visual browsing over hierarchical navigation
- **Referential Architecture**: Maintains pointers to files rather than requiring specific organization
- **Metadata Enhancement**: Enriches assets with additional information independent of filesystem capabilities

This contrasts with traditional folder-based approaches where organization and storage are intrinsically linked. Understanding this distinction explains why "collections" exist separately from the assets themselves.

### Typeface's Font Management Paradigm

Typeface's approach to font management demonstrates why fonts receive special treatment:
- **Activation Model**: Manages font availability to the system rather than just organization
- **Metadata-Rich Categorization**: Organizes by attributes beyond what filesystem hierarchies can represent
- **Preview-Centric Interface**: Prioritizes visual representation over filename or location
- **Parallel Organization**: Maintains its own categorization separate from filesystem structure

These specialized needs underscore why font management often exists outside traditional file organization schemes.

### Collections vs. Assets Separation

The architectural distinction between collections and assets reflects fundamental differences in purpose:
- **Content vs. Organization**: Assets are the artifacts themselves; collections are ways of understanding them
- **Physical vs. Logical**: Assets occupy storage space; collections represent organizational views
- **Persistence vs. Fluidity**: Assets remain relatively stable; organizational schemes evolve
- **Single vs. Multiple**: An asset exists once; it may belong to multiple organizational schemes

This separation enables multiple organizational perspectives on the same underlying content—a powerful concept that transcends the limitations of folder hierarchies.

## Terminology Architecture

### "Libraries" as a Conceptual Challenge

The term "libraries" creates cognitive friction for several architectural reasons:
- **Semantic Overloading**: Already heavily used in macOS (~/Library), programming contexts, and design systems
- **Representational Ambiguity**: Suggests both the content and the organizational scheme
- **Conceptual Imprecision**: Fails to differentiate between files and their organizational metadata

Alternative conceptual models might include:
- **Catalogs**: Emphasizes indexing and retrieval functions
- **Collections**: Focuses on curatorial aspects of organization
- **Indexes**: Highlights the referential nature of asset organization

### Cognitive Load in Information Architecture

Terminology serves as the interface between mental models and file systems. Reducing cognitive load requires:
- **Domain Appropriateness**: Terms should align with how you think about your work
- **Contextual Differentiation**: Each term should occupy a distinct semantic space
- **Hierarchical Clarity**: Naming should reflect the relationship between concepts
- **Functional Transparency**: Terms should suggest the purpose of each directory

The goal isn't merely simplification but alignment with your thought processes and workflows.

## Structural Refinement Principles

### Organizational Ordering Approaches

Alphabetical ordering represents one of several possible organizational principles:
- **Findability vs. Relationship**: Alphabetical ordering optimizes for finding specific items but may separate related concepts
- **Usage Patterns vs. Consistency**: Frequency-based ordering reflects workflows but requires maintenance
- **Cognitive Mapping**: The ideal order should match how you mentally categorize your work
- **Mixed Approaches**: Different sections might benefit from different ordering principles

The best approach depends on whether you primarily search for specific folders or navigate between related ones.

### Work Folder Conceptual Placement

The Work folder's position reflects a fundamental tension in directory architecture:
- **Access Frequency**: Top-level placement provides immediate access
- **Conceptual Grouping**: Moving under Documents would group it with other personal information
- **Functional Independence**: Current placement suggests distinct purpose from Projects
- **Mental Categorization**: Optimal placement depends on how you conceptualize this content

The decision hinges on whether "Work" represents an access-frequency-driven category or a conceptual grouping within personal documents.

### Architectural Optimization Philosophy

Directory structure optimization balances competing principles:
- **Depth vs. Breadth**: Shallower structures reduce navigation complexity but increase choice complexity
- **Grouping vs. Findability**: Logical grouping improves understanding but may hide specific items
- **Consistency vs. Specialization**: Uniform patterns aid learning but miss domain-specific needs
- **Physical vs. Logical**: Organization can reflect storage realities or abstract concepts

Effective architectures harmonize these tensions rather than resolving them completely.

## Symlink Directionality Theory

### Conceptual Model of Symlink Direction

Symlink direction embodies a fundamental architectural decision about primacy:
- **Source → Target Relationship**: Which location conceptually "owns" the content?
- **Change Propagation**: Where do changes originate and how are they reflected?
- **Resilience Characteristics**: How does the system behave when components are unavailable?
- **Backup Implications**: How do backup systems interpret and preserve the relationship?

Cloud → Local symlinking (our recommendation) establishes the cloud location as authoritative, with local organization providing convenient access views.

### Functional Implications of Direction Choice

The direction choice creates distinct architectural behaviors:
- **Authority Model**: Cloud → Local establishes cloud storage as the "source of truth"
- **Failure Modes**: Links break differently depending on which end becomes unavailable
- **Sync Behavior**: Cloud services handle their own content more reliably than symlinked content
- **Reorganization Flexibility**: Direction determines which side can be reorganized without breaking links

This architectural decision fundamentally shapes how your system behaves during changes, synchronization, and recovery scenarios.

Would you like me to explore any of these architectural principles in more depth? I can further examine specific aspects of the directory structure through these conceptual lenses.

# My Position on Directory Architecture Concepts

You've got it exactly right about assets and libraries! Your book analogy is perfect - assets are the books themselves, while the catalogue (library) is the system organizing them. A single book can appear in multiple cataloguing systems without being duplicated.

## On Terminology Choices

I'm actually not neutral on this - I strongly prefer "Catalogue" over "Library" for your structure. "Library" creates too much confusion with macOS's system Library, and "Collection" does imply the items themselves rather than the organizational system. "Catalogue" clearly communicates "this is how we find and organize things" rather than "this is the stuff itself."

Reserving "Index" for other purposes makes sense - it has technical connotations that might be valuable elsewhere.

## Resources, References, and Assets Hierarchy

This is an area where I have definite opinions based on information architecture principles:

```
~/
├── Resources/       # Container for all supportive materials
│   ├── Assets/      # Design/media elements used in projects
│   ├── Templates/   # Starting points for new work
│   ├── Catalogues/  # Organization systems for resources
│   └── References/  # Information consulted but rarely modified
```

My recommendation is to keep Assets *within* Resources because:
1. **Conceptual Clarity**: Assets are a type of resource - this creates a clean mental model
2. **Expansion Flexibility**: As you add new resource types, the organization remains logical
3. **Consistent Depth**: Keeps critical folders at the same level in your hierarchy

For desktop wallpapers specifically - I consider these to be assets with a specific purpose. I'd place them at `~/Resources/Assets/Wallpapers/` rather than mixing concerns by putting them in a system folder.

## A Better High-Level Organization

Based on our discussion, here's what I believe is the strongest overall architecture:

```
~/                      # Home directory
├── Projects/           # Work you're actively creating
├── Resources/          # Materials that support your work
├── Knowledge/          # Information you've collected or created
├── System/             # Computer management and configuration
├── Documents/          # Personal information (including Work/)
│   └── Work/           # Work-related documents
└── ... (standard macOS folders)
```

This provides clear separation of concerns while maintaining logical grouping. Each top-level folder has a distinct purpose that's immediately understandable.

## On Symlink Direction

While I presented multiple perspectives, I have a strong preference for cloud → local symlinks because:
1. It establishes cloud storage as the "source of truth"
2. Handles sync conflicts more gracefully
3. Ensures backups capture the authoritative version
4. Allows local reorganization without affecting cloud storage

## My Personal Take

If I were implementing this system for myself, I'd:
1. Use "Catalogue" instead of "Library" to avoid confusion
2. Keep Assets within Resources for conceptual clarity
3. Move Work under Documents to simplify top-level structure
4. Maintain a strict cloud → local symlink direction
5. Organize by purpose first, then by file type (not the reverse)

The most important principle is that your directory structure should mirror how you think about your work. If you mentally categorize assets as a distinct top-level concept separate from other resources, then that organization might work better for you personally, despite the architectural advantages of the nested approach.

What aspects of this structure are you leaning toward implementing first?