# FOMO Controlled Vocabulary: Modular Revision Plan

## 1. Modular Documentation Framework

### Purpose
To transform the existing monolithic controlled vocabulary document into a cohesive system of interconnected modules that enhance usability, maintainability, and practical implementation while preserving complete coverage of terminology standards across the FOMO system.

### Modular Structure Overview

**Core Document**:
- **fomo-controlled-VOCABULARY-v02.md**: Framework, principles, governance, and document map

**Satellite Documents** (in priority order):
1. **fomo-term-DICTIONARY-v01.md**: Complete alphabetical listing of all approved terms
2. **fomo-term-CHEATSHEET-v01.md**: One-page quick reference of essential terms
3. **fomo-vocabulary-EXTENSIONS-design-v01.md**: Design-specific terminology and workflows
4. **fomo-vocabulary-EXTENSIONS-development-v01.md**: Development-specific terminology
5. **fomo-vocabulary-IMPLEMENTATION-GUIDE-v01.md**: Practical adoption strategies
6. **fomo-vocabulary-MAPS-v01.md**: Visual relationship diagrams and decision flows

## 2. Document Specifications

### 2.1 Core Document: Controlled Vocabulary Framework

**Purpose**: Establish the governing principles, structure, and maintenance procedures for the entire vocabulary system.

> `fomo-controlled-VOCABULARY-v##.md`

**Key Sections**:
- Introduction and purpose of controlled vocabulary in FOMO
- Core principles and implementation philosophy
- Category system and terminology organisation
- Term formatting standards and conventions
- Document map explaining the modular ecosystem
- Governance model and maintenance procedures
- Integration with other FOMO components
- Future growth framework

**Enhancement Implementation**:
- **Clear Boundaries**: Include explicit "do not use" section with examples and rationales
- **Transition Strategy**: High-level migration approach from current to new system
- **Visual Components**: Framework for visual elements across all documents
- **Cross-Document Integration**: Explicit mapping to other FOMO standards

**Development Notes**:
- Reduce overall length by moving detailed listings to satellite documents
- Focus on principles and structure rather than exhaustive listings
- Include clear cross-references to all satellite documents
- Provide governance model for the entire vocabulary ecosystem

### 2.2 Primary Satellite: Term Dictionary

**Purpose**: Serve as the detailed reference for all approved terms in an accessible format.

> `fomo-term-DICTIONARY-v##.md`

**Key Sections**:
- Alphabetical master listing of all terms
- Consistent entry format:
  - Term
  - Definition
  - Category (Project, Resource, Knowledge, System, etc.)
  - Priority level (••• for essential, •• for important, • for specialised)
  - Format example
  - Usage context
  - Related terms

**Enhancement Implementation**:
- **Dictionary Accessibility**: Alphabetical organisation with category indicators
- **Visual Hierarchy**: Format distinction between essential and specialised terms
- **Real-World Usage Examples**: Practical examples for each term
- **Domain Relevance**: Tags indicating relevant domains for cross-specialty terms

**Development Notes**:
- Extract and enhance existing dictionary entries from current document
- Add priority indicators to all terms
- Ensure consistent formatting across all entries
- Include cross-references to domain-specific extensions where relevant

### 2.3 Primary Satellite: Term Cheatsheet

**Purpose**: Provide a printable quick-reference guide focusing on essential terminology.

> `fomo-term-CHEATSHEET-v##.md`

**Key Sections**:
- Core terms organised by category
- Essential formatting rules
- Common term combinations
- Workflow-based groupings
- Quick decision guide

**Enhancement Implementation**:
- **Visual Hierarchy**: Colour-coding or formatting to distinguish term types
- **Real-World Usage**: Concise examples of common applications
- **Domain Integration**: Visual indicators for domain crossover terms

**Development Notes**:
- Limit to one page (two sides maximum)
- Focus exclusively on high-priority (•••) terms
- Use visual elements to enhance scannability
- Optimise for both digital reference and printing

### 2.4 Extension Documents: Domain-Specific Modules

**Purpose**: Provide detailed guidance for specialised domains while maintaining system-wide consistency.

> `fomo-vocabulary-EXTENSIONS-design-v##.md`

**Design Extension Key Sections**:
- Design-specific terminology
- Design state and workflow terms
- Asset classification and naming
- Client delivery terminology
- Design-to-development handoff terms

> `fomo-vocabulary-EXTENSIONS-development-v##.md`

**Development Extension Key Sections**:
- Development-specific terminology
- Language-specific naming conventions
- Component and architecture terms
- Development stages and states
- Technical specification terminology

**Enhancement Implementation**:
- **Domain-Specific Content**: Preserve and enhance existing specialised terminology
- **Cross-Domain Workflows**: Document terminology transitions between domains
- **Real-World Examples**: Include actual workflow scenarios for each domain

**Development Notes**:
- Build upon existing domain-specific extensions
- Add priority indicators for domain-specific terms
- Include practical cross-domain workflows
- Maintain consistency with core terminology principles

### 2.5 Supporting Document: Implementation Guide

**Purpose**: Provide practical strategies for adopting the controlled vocabulary across existing workflows.

> `fomo-vocabulary-IMPLEMENTATION-GUIDE-v##.md`

**Key Sections**:
- Step-by-step implementation approach
- Before/after migration examples
- Automation integration instructions
- Common scenarios with solutions
- Validation and compliance checking

**Enhancement Implementation**:
- **Transition Strategy**: Detailed guidance for migration from current practices
- **Automation Support**: Instructions for integration with existing FOMO tools
- **Practical Testing**: Validation methods for terminology compliance

**Development Notes**:
- Focus on practical, actionable guidance
- Include specific procedures for different file types and workflows
- Provide examples that demonstrate immediate benefits
- Include troubleshooting guidance for common issues

### 2.6 Supporting Document: Visual Relationship Maps

**Purpose**: Enhance understanding of term relationships and selection processes through visual representation.

> `fomo-vocabulary-MAPS-v##.md`

**Key Sections**:
- Category relationship diagrams
- Term selection decision trees
- Workflow visualisations
- Domain crossover maps

**Enhancement Implementation**:
- **Visual Components**: Specific formats for different relationship types
- **Cross-Domain Integration**: Visual mapping of term relationships across domains
- **Term Relationships**: Clear visual representation of hierarchies and associations

**Development Notes**:
- Use Mermaid diagrams for compatibility with markdown
- Provide alternative formats where appropriate
- Focus on clarity over complexity
- Include interpretive text with all visual elements

## 3. Development Strategy

### 3.1 Phase 1: Essential Foundations (Immediate Priority)

**Deliverables**:
1. Term Dictionary (v01)
2. Term Cheatsheet (v01)
3. Core Vocabulary Framework (v02)

**Approach**:
- Extract and enhance existing dictionary entries
- Create priority system (•••, ••, •)
- Develop one-page cheatsheet of essential terms
- Restructure core document to serve as framework
- Establish cross-referencing system between documents

**Success Criteria**:
- Complete alphabetical listing of all terms
- Consistent formatting across all entries
- Printable one-page cheatsheet
- Clear framework document with reduced length
- Working cross-reference system

### 3.2 Phase 2: Domain Extensions (Medium Priority)

**Deliverables**:
1. Design Extension Document (v01)
2. Development Extension Document (v01)

**Approach**:
- Extract domain-specific content from original document
- Enhance with additional domain-specific examples
- Add workflow processes showing terminology progression
- Create cross-domain terminology mappings
- Ensure consistency with core vocabulary principles

**Success Criteria**:
- Comprehensive domain-specific terminology
- Clear workflows using standardised terms
- Effective cross-domain mappings
- Consistency with core vocabulary framework

### 3.3 Phase 3: Practical Application (Medium Priority)

**Deliverables**:
1. Implementation Guide (v01)

**Approach**:
- Develop practical transition strategies
- Create before/after examples
- Document automation integration methods
- Include validation procedures
- Provide troubleshooting guidance

**Success Criteria**:
- Clear migration path from current to new system
- Working examples demonstrating benefits
- Functional automation integration
- Effective validation methods

### 3.4 Phase 4: Visual Enhancement (Lower Priority)

**Deliverables**:
1. Visual Relationship Maps (v01)

**Approach**:
- Identify key relationships for visualisation
- Develop appropriate diagram formats
- Create decision trees for term selection
- Document cross-domain visual mappings

**Success Criteria**:
- Clear, usable visualisations
- Enhanced understanding of term relationships
- Effective decision support tools
- Compatibility with markdown format

## 4. Implementation of Enhancement Suggestions

### 4.1 Preserve Dictionary Accessibility
- Maintain alphabetical master list in Term Dictionary
- Add category indicators while preserving a-z access
- Include quick-jump alphabet navigation
- Provide consistent entry format for all terms

### 4.2 Enhance Domain-Specific Content
- Create dedicated extension documents for each domain
- Preserve all existing domain-specific terminology
- Add practical cross-domain workflows
- Develop terminology mappings between domains

### 4.3 Clarify Visual Components
- Specify exact formats for visual elements
- Use Mermaid for relationship diagrams
- Create dedicated Visual Maps document
- Include interpretive text with all visuals

### 4.4 Maintain Clear Boundaries
- Include explicit "what not to do" guidelines in core document
- Provide examples of common mistakes
- Include rationales for boundaries
- Add visual distinction for prohibited practices

### 4.5 Real-World Usage Examples
- Include practical examples for all terms
- Add workflow-based examples showing term progression
- Provide before/after comparisons
- Include actual file naming examples

### 4.6 Address Transition Strategy
- Create dedicated Implementation Guide
- Include specific migration procedures
- Provide guidance for legacy content
- Develop compliance validation methods

## 5. Implementation of Practical Considerations

### 5.1 Section Ordering
- Place Term Dictionary as a standalone document for easy reference
- Organise core document with principles first, details later
- Structure each document with most-used information at the beginning
- Use consistent section ordering across all documents

### 5.2 Cheatsheet Creation
- Develop standalone, printable Term Cheatsheet
- Focus exclusively on high-priority terms
- Optimise layout for both digital and print use
- Include essential formatting rules

### 5.3 Visual Hierarchy
- Implement priority indicators (•••, ••, •) consistently
- Use formatting to distinguish between term types
- Apply colour-coding or visual markers for quick identification
- Maintain consistent visual language across all documents

### 5.4 Cross-Document Integration
- Establish explicit connections to Directory Structure Guidelines
- Ensure alignment with Naming Standards
- Create clear cross-references between vocabulary documents
- Maintain terminology consistency with all FOMO documentation

### 5.5 Practical Testing
- Include validation methods in Implementation Guide
- Develop basic script concepts for terminology compliance checking
- Create manual audit procedures
- Include specific test cases for various file types

## 6. Document Integration Procedures

### 6.1 Cross-Referencing System
- Standard format: "See [Document Name] for [specific information]"
- Hyperlinks in digital versions where possible
- Page references for printable documents
- Visual indicators for external references

### 6.2 Version Control
- Coordinate version numbers across related documents
- Document dependencies in version history
- Update cross-references when versions change
- Maintain changelog in FOMO Maintenance Log

### 6.3 Consistency Verification
- Regular cross-document audits
- Terminology alignment checks
- Formatting consistency verification
- Reference validation

### 6.4 Future Updates Procedure
- Define update triggers for each document
- Establish review process for terminology additions
- Document ripple effect identification
- Create update sequence for multi-document changes

## 7. Success Metrics

### 7.1 Usability Metrics
- Time to locate specific term information
- User confidence in term selection
- Error rate in terminology application
- User satisfaction ratings

### 7.2 Integration Metrics
- Alignment with other FOMO standards
- Successful automation implementation
- Cross-domain workflow effectiveness
- System-wide terminology consistency

### 7.3 Maintenance Metrics
- Efficiency of update process
- Documentation currency
- User feedback implementation
- Error correction speed

### 7.4 Practical Application Metrics
- Terminology adoption rate
- Compliance percentage for new files
- Reduction in naming decision time
- Automation success rate

## 8. Next Steps and Action Items

### 8.1 Immediate Actions
1. Extract and organise all terms from existing document
2. Assign priority levels to all terms
3. Draft Term Dictionary document structure
4. Create one-page Cheatsheet layout
5. Restructure core Framework document

### 8.2 Technical Requirements
1. Mermaid diagram integration for workflow visualisations
2. Consistent markdown formatting templates for all documents
3. Sample scripts for terminology validation
4. Cross-reference tracking system

### 8.3 Integration Actions
1. Review all FOMO standards documents for terminology alignment
2. Identify terminology inconsistencies across current documentation
3. Create term mapping between current and new systems
4. Develop transition timeline aligned with FOMO implementation phases

---

*Version History:*
- v01 - 2025-04-01: Initial modular revision plan created