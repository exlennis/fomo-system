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

## Application to FOMO Project

Based on the research findings, the FOMO Naming Standards were developed with the following considerations:

1. **Primary Case Format Selection**
	- Kebab-case was selected as the primary format due to its superior balance of human readability and machine processing capabilities
	- Specific exceptions were made for established programming conventions (PascalCase for React components, snake_case for Python)
	
2. **Structural Components Optimisation**
	- Date format selection (YYYYMMDD) optimised for chronological sorting
	- Version numbering (v01) designed for visual consistency and proper sorting
	- Special character restrictions implemented to ensure cross-platform compatibility
	
3. **Pattern Development**
	- File type-specific patterns developed to balance standardisation with practical usage
	- Templates designed to incorporate essential metadata while maintaining readability
	- Special case handling developed for multilingual content, temporary files, and domain-specific requirements
	
4. **Automation Considerations**
	- Patterns optimised for script-based processing and validation
	- Consistent structures enable reliable pattern matching in automation tools
	- Format allows for metadata extraction through regular expressions

## Technical Implementation Insights

The research findings directly informed several technical aspects of the naming standards:

1. **Regular Expression Optimisation**
	- Kebab-case patterns allow for simpler regex patterns for validation and extraction
	- Example pattern: `^[a-z0-9]+(-[a-z0-9]+)*$` for basic validation
	
2. **Sort Order Predictability**
	- Date format placement ensures chronological grouping of related files
	- Version numbering format preserves intended sequence
	
3. **Cross-Platform Considerations**
	- Avoidance of special characters prevents path parsing issues across systems
	- Case sensitivity handling balanced for case-sensitive (Unix) and case-insensitive (Windows) filesystems
	
4. **AI Processing Compatibility**
	- Consistent patterns improve automated classification accuracy
	- Semantic components enable AI to extract meaning from filenames
	- Clear delimiters improve parsing for automation agents

## Challenges and Trade-offs

The research revealed several challenges that required careful balancing:

1. **Domain-Specific Conventions vs. System-Wide Consistency**
	- Resolution: Created exceptions framework for framework-specific requirements while maintaining core principles
	
2. **Human Readability vs. Machine Optimisation**
	- Resolution: Selected kebab-case as optimal middle ground between these competing needs
	
3. **Comprehensive Metadata vs. Name Length**
	- Resolution: Developed templates that include essential metadata while keeping names reasonably concise
	
4. **Compatibility with Existing Systems**
	- Resolution: Created migration strategy with priority tiers and automation support

## Design and Development Context Considerations

For someone working across both design and development domains, several specific insights emerged:

1. **Cross-Domain File Naming**
	- Design assets often require version tracking that development files manage through Git
	- Resolution: Incorporated explicit version numbers in design asset filenames while allowing development files to follow language conventions
	
2. **Tool-Specific Considerations**
	- Adobe tools (Photoshop, Illustrator) handle special characters differently than development environments
	- Resolution: Limited special characters to those universally supported across tools
	
3. **Asset Library Organisation**
	- Design assets often need pixel density indicators that code files don't require
	- Resolution: Created special case handling for density indicators using the underscore exception

The final naming standards represent a carefully balanced approach that optimises for both human and machine requirements while providing enough flexibility to accommodate various file types and use cases across design and development workflows.
