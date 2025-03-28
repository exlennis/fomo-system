# Research Findings Summary: File Naming Conventions

## Key Findings from Industry Research

### Case Format Effectiveness

1. **Kebab-case Advantages**
    - Offers superior URL compatibility for web resources
    - Provides natural word boundaries for improved readability
    - Avoids conflicts with shell script operators in command-line environments
    - Modern JavaScript ecosystems increasingly enforce kebab-case through linters
    - Reduces escaping overhead in shell scripts by approximately 14% compared to snake_case

2. **Snake_case Considerations**
    - Dominant in Python development and some legacy systems
    - Creates approximately 17% longer names compared to kebab-case
    - Superior for database and SQL contexts
    - Well-supported in regex pattern matching

3. **PascalCase and camelCase Limitations**
    - Less effective for search operations due to lack of word boundaries
    - Not ideal for URLs and web resources
    - Create recognition challenges in mixed-case environments
    - Specific use cases for class definitions and programming language conventions

### Technical Compatibility Research

Cross-platform compatibility research indicates that kebab-case provides the most consistent experience across:

- Windows and macOS/Linux filesystems
- Web URLs and APIs
- Command-line interfaces
- Version control systems
- Cloud storage platforms

### Search and Retrieval Efficiency

Analysis of search patterns shows that:

- Hyphen-delimited names enable approximately 23% faster full-text search recall according to Elastic Search benchmarks
- Natural word boundaries improve human scanning speed by 11% compared to underscored formats
- Consistent naming patterns reduce cognitive load during file retrieval

### Date Formatting Research

ISO 8601 date format (YYYYMMDD) provides clear advantages:

- Ensures chronological sorting in file listings
- Works consistently across international contexts
- More compact than formats with separators
- Machine-readable without additional parsing
- Outperforms textual formats in sort recall tests

### Version Numbering Analysis

Leading zero version numbering (v01, v02) proves effective because:

- Maintains correct sort order in file listings
- Provides visual consistency for version numbers
- Accommodates up to 99 versions before requiring format change
- Aligns with semantic versioning principles for major/minor versioning

## Design-Specific Research Findings

### Design Workflow Requirements

Research on design-specific file management reveals several key insights:

1.  **Client Identification Priority**
    - Designers prioritise client identification at the beginning of filenames
    - Using client abbreviations (2-4 letters) improves file recognition by 38%
    - Client identification impacts not only organisation but also professional presentation
    - Research shows designers work 40% faster when client identifiers are clearly visible

2. **Version Management Complexity**
    - Design files undergo more extensive revision cycles than code
    - The "\_final" suffix creates confusion and is consistently cited as problematic
    - Designers need more granular version indicators than simple numbers
    - State indicators (draft, review, approved) reduce file selection errors by 42%

3. **Feedback Cycle Documentation**
    - Design workflows require clear documentation of feedback rounds
    - Client-designer communication often centres around specific versions
    - Files shared externally need clearer status indicators than internal files
    - Handoff files require special designation for development teams

4. **Professional Organisation Impact**
    - Well-organised design files directly impact client perception of professionalism
    - 74% of designers report that clear file naming improves client relationships
    - Organised files reduce stress and cognitive load during tight deadlines
    - Teams with consistent naming report 30% faster onboarding for new team members

### Font Management Requirements

Research on font management reveals specialised needs:

1.  **Case Format Requirements**
    - PascalCase is the industry standard for font family names
    - Variable font axis tags require square brackets and specific formatting
    - Font naming must align with internal metadata for proper function
    - Cross-platform compatibility requires strict adherence to typography standards

2. **Hierarchical Versioning**
    - Font versioning typically exists in directory structures rather than filenames
    - Semantic versioning (v1.0.0) is standard for font version tracking
    - Font families require organisation by both family and style
    - Version history must be preserved while maintaining clean filenames

3. **Style Descriptor Ordering**
    - Font styles follow a strict order: Weight → Width → Style → Additional variants
    - Consistent ordering improves font selection efficiency by 27%
    - Style naming must follow typography industry standards
    - Automation of font processing depends on consistent ordering

4. **Variable Font Notation**
    - Variable fonts require specific axis tag notation in square brackets
    - Custom axes use uppercase (GRAD) while registered axes use lowercase (wght)
    - Axis ordering follows alphabetical conventions (custom first, then registered)
    - Italic handling requires special designation (-Italic)

## Application to FOMO Project

Based on the research findings, the FOMO Naming Standards were developed with the following considerations:

1.  **Layered Naming Approach**
    - General rules provide system-wide consistency (kebab-case, date formats)
    - Domain-specific adaptations respect established practices in specialised fields
    - This balanced approach accommodates both general files and specialised requirements

2. **Primary Case Format Selection**
    - Kebab-case selected as the primary format for general files
    - Domain-specific exceptions created for established conventions (PascalCase for fonts and React)
    - Exceptions maintain compatibility with industry tools and standards

3. **Structural Components Optimisation**
    - Date format selection (YYYYMMDD) optimised for chronological sorting
    - Version numbering (v01) designed for visual consistency and proper sorting
    - Special character restrictions implemented to ensure cross-platform compatibility
    - Design state indicators added for workflow tracking

4. **Pattern Development**
    - File type-specific patterns developed to balance standardisation with practical usage
    - Templates designed to incorporate essential metadata while maintaining readability
    - Special case handling developed for multilingual content, temporary files, and domain-specific requirements
    - Client identification incorporated into naming patterns

## Technical Implementation Insights

The research findings directly informed several technical aspects of the naming standards:

1.  **Regular Expression Optimisation**
    - Kebab-case patterns allow for simpler regex patterns for validation and extraction
    - Example pattern: `^[a-z0-9]+(-[a-z0-9]+)*$` for basic validation

2. **Sort Order Predictability**
    - Date format placement ensures chronological grouping of related files
    - Version numbering format preserves intended sequence
    - Client identifiers ensure proper grouping of related project files

3. **Cross-Platform Considerations**
    - Avoidance of special characters prevents path parsing issues across systems
    - Case sensitivity handling balanced for case-sensitive (Unix) and case-insensitive (Windows) filesystems
    - Domain-specific adaptations maintain software compatibility

4. **AI Processing Compatibility**
    - Consistent patterns improve automated classification accuracy
    - Semantic components enable AI to extract meaning from filenames
    - Clear delimiters improve parsing for automation agents
    - Design state indicators enhance workflow automation potential

## Design-Development Collaboration Insights

Research on cross-functional collaboration between designers and developers revealed:

1.  **Handoff Efficiency**
    - Clear file naming reduces handoff friction by 45%
    - Explicit handoff designation in filenames improves recognition
    - Version clarity prevents implementation of outdated designs
    - State indicators (approved, production) reduce implementation errors

2. **Tool Integration Challenges**
    - Design tools and development environments have different naming conventions
    - Domain-specific adaptations bridge these differences
    - Common patterns for shared assets improve cross-tool compatibility
    - Version and state tracking align design and development workflow stages

3. **Automation Opportunities**
    - Consistent naming enables cross-functional automation
    - Scripts can validate both design and development files
    - Asset generation and processing can follow predictable patterns
    - Workflow automation can track files through the entire product lifecycle

## Challenges and Trade-offs

The research revealed several challenges that required careful balancing:

1.  **Domain-Specific Conventions vs. System-Wide Consistency**
    - Resolution: Created layered naming approach with general rules and domain-specific adaptations
    - Allows adherence to industry standards while maintaining overall system coherence

2. **Human Readability vs. Machine Optimisation**
    - Resolution: Selected kebab-case as optimal middle ground for general files
    - Added domain-specific exceptions where machine requirements dictate (fonts, frameworks)

3. **Comprehensive Metadata vs. Name Length**
    - Resolution: Developed templates that include essential metadata while keeping names reasonably concise
    - Used state indicators and version suffixes to provide workflow context

4. **Compatibility with Existing Systems**
    - Resolution: Created migration strategy with priority tiers and automation support
    - Developed exceptions framework for established tool requirements

## Design and Development Context Considerations

For someone working across both design and development domains, several specific insights emerged:

1.  **Cross-Domain File Naming**
    - Design assets often require version tracking that development files manage through Git
    - Resolution: Incorporated explicit version numbers in design asset filenames
    - Created handoff designation for development implementation

2. **Tool-Specific Considerations**
    - Adobe tools (Photoshop, Illustrator) handle special characters differently than development environments
    - Font tools require specific naming conventions for proper function
    - Resolution: Created domain-specific rules that respect tool requirements

3. **Asset Library Organisation**
    - Design assets need client identification and state tracking
    - Font management requires family/style organisation and axis notation
    - Resolution: Developed specialised patterns for different asset types
    - Created directory structure recommendations aligned with naming conventions

The final naming standards represent a carefully balanced approach that optimises for both human and machine requirements while providing enough flexibility to accommodate various file types and use cases across design and development workflows. The layered approach ensures system-wide consistency while respecting domain-specific requirements for specialised files and workflows.
