# AI File Renaming: Balancing Pre-developed Tools and AI Solutions

## Project Context

This document outlines the framework and approach for building an AI-powered file renaming system that leverages Warp Terminal's Agent Mode. Based on findings from our initial implementation and testing, we're focusing on creating a balanced ecosystem of pre-built utilities and AI-directed processes.

The goal is for AI agents to analyse the file contents along with a systematic renaming scheme that makes each file’s purpose and functionality clear at a glance

## Core Philosophy

The ideal system combines:
1. **Modular pre-built utilities** that handle common, repeatable tasks efficiently
2. **AI-directed orchestration** that makes intelligent decisions about naming strategies
3. **Contextual awareness** that considers directory-wide patterns and file relationships

## Pre-developed Utility Modules

These small, focused utilities provide reliable building blocks that the AI can combine and customize:

### File Processing Utilities
- `extract_content [file] [options]` - Extract readable content from various file types
- `get_metadata [file] [options]` - Extract metadata (creation date, title, author)
- `sample_content [file] [length]` - Get representative content sample for analysis

### String Manipulation
- `clean_string [string] [options]` - Remove/replace special characters, emojis, etc.
- `format_case [string] [style]` - Convert to kebab-case, camel-case, snake_case, etc.
- `truncate_smart [string] [length]` - Intelligently truncate while preserving meaning

### Analysis Tools
- `identify_common_prefixes [files]` - Find repeated prefixes across multiple files
- `extract_keywords [content]` - Extract meaningful keywords from text
- `detect_versioning [filename]` - Identify version patterns (v1, draft, final, etc.)

### Conflict Resolution
- `check_conflicts [directory] [names]` - Detect potential naming conflicts
- `resolve_conflict [name] [existing] [strategy]` - Apply conflict resolution strategy

## AI Decision Framework

Rather than prescribing exactly how files should be renamed, we provide a framework for AI to make informed decisions:

### Analysis Phase
1. Scan directory for patterns and relationships
2. Create content fingerprints for each file
3. Identify distinguishing features of similar files
4. Detect important naming conventions already in use

### Decision Matrix
A structured approach for determining the best naming strategy:

| Content Type | Primary Strategy | Fallback Strategy | Preservation Rules |
|--------------|-----------------|-------------------|-------------------|
| Documents    | Extract title   | Content summary   | Keep version info |
| Code         | Project + function | Functionality description | Keep language extension |
| Data files   | Dataset + date  | Content type + source | Keep date info |
| Media        | Subject + date  | Location + timestamp | Keep creator info |

### Conflict Resolution Strategies
1. **Content comparison** - Before renaming, compare file content with tools like `diff` to identify:
   - Identical duplicates (safe to mark for archiving or removal)
   - Near-duplicates with minor differences (highlight differences for user review)
   - Similar files with significant differences (require distinct names)

2. **Add distinguishing context** - Incorporate unique aspects from content:
   - For similar documents, extract distinguishing topics or sections
   - Use creation/modification dates if content differs temporally
   - Include author or source information if available in metadata

3. **Preserve original uniqueness** - Maintain differentiating parts of original name:
   - Retain version numbers, dates, or qualifiers (draft, final, etc.)
   - Keep unique identifiers like project codes or timestamps
   - Preserve distinguishing prefixes or suffixes from original names

4. **Add numbering** - Sequential suffix when content is truly similar:
   - Use semantic numbering where possible (part1, part2 rather than just 1, 2)
   - Include date-based sequence for temporal content
   - Consider content-based ordering rather than arbitrary assignment

5. **Hierarchical naming** - Include parent folder context in ambiguous cases:
   - Incorporate project or category name from directory structure
   - Use breadcrumb-style prefixes for deeply nested content
   - Reference related files in naming strategy

## Implementation Considerations

### Testing Framework
- Test with diverse file collections (docs, code, mixed content)
- Measure naming quality (descriptiveness, uniqueness, brevity)
- Track conflict resolution success rate
- Validate deduplication accuracy with intentionally duplicated files

### Performance Optimization
- Cache content extraction results
- Process files in batches
- Optimize for large directories
- Implement efficient content comparison algorithms (checksums for quick identical matching)

### User Experience
- Provide clear preview of proposed changes
- Group similar files for batch decisions
- Allow selective application of changes
- Present detailed diff outputs for near-duplicates
- Create summary logs of duplicate files identified and actions taken

### Duplicate Handling
- **Detection Methods**:
  - Quick check: File size and checksums/hashes (MD5, SHA-1)
  - Deep check: Full content comparison with `diff`
  - Smart check: Semantic similarity for text documents
  
- **Action Options**:
  - Log duplicates with clear indication in reports
  - Move duplicates to archive directory
  - Option to automatically delete exact duplicates (with appropriate safeguards)
  - Preserve newest version based on metadata
  
- **Documentation**:
  - Record all duplicate handling in detailed logs
  - Create manifest of duplicate sets
  - Maintain audit trail of actions taken

## Implementation Plan

### Phase 1: Core Utilities Development
1. **File Analysis Tools** (Core Utilities)
   - `file_utilites.sh` - Type detection, metadata extraction
   - `content_utilites.sh` - Content extraction, title/keyword parsing
   - `string_utilites.sh` - Case formatting, smart truncation
   - `directory_utilites.sh` - Pattern analysis, duplicate detection

2. **Integration Layer**
   - `rename_utilites.sh` - Main logic for coordinating renaming operations
   - `ai_integration.sh` - Prompt template management and AI response handling

3. **Command-line Interface**
   - `ai-rename.sh` - User-friendly entry point with argument handling
   - `config.sh` - Configuration management

### Phase 2: Testing Framework
1. **Test Directory Generation**
   - Create diverse test file sets with known patterns and challenges
   - Include common edge cases (special characters, duplicates, collisions)

2. **Validation Scripts**
   - `test_content_extraction.sh` - Verify content sampling
   - `test_duplicate_detection.sh` - Confirm duplicate identification
   - `test_collision_handling.sh` - Ensure safe renaming

3. **Performance Testing**
   - Test with large file sets (100+ files)
   - Optimize processing for batches and parallelization

### Phase 3: AI Integration
1. **Prompt Engineering**
   - Design templates for different AI models
   - Create context-aware prompt formats

2. **Response Parsing**
   - Develop robust parsers for structured AI responses
   - Handle error cases and unexpected AI outputs

3. **Warp Terminal Integration**
   - Optimize workflow for Warp Terminal Agent Mode
   - Create interactive guidance system

### Phase 4: Refinement and Documentation
1. **User Documentation**
   - Installation guides
   - Usage examples
   - Troubleshooting

2. **Developer Documentation**
   - Architecture overview
   - API documentation
   - Extension guidelines

## Testing Strategy

1. **Unit Testing**
   - Test each utility function individually
   - Verify correct handling of edge cases
   - Ensure cross-platform compatibility (macOS, Linux)

2. **Integration Testing**
   - Test full workflow end-to-end
   - Validate interaction between modules
   - Test with different AI models

3. **User Acceptance Testing**
   - Test with real-world file collections
   - Gather feedback on naming quality
   - Measure speed and efficiency improvements

## Resources and References

- Original [ai-renamer](https://github.com/excalidraw/ai-renamer) project
- Warp Terminal API documentation
- File naming convention standards
- Natural language processing techniques for content summarisation
- [Raycast script repository](https://github.com/raycast/script-commands) for utility script patterns
