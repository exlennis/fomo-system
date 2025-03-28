# Comparison of Naming Approaches

| Criteria | Kebab-case | Snake_case | PascalCase | camelCase |
|----------|------------|------------|------------|-----------|
| **Human Readability** | Excellent - Natural word breaks with hyphens | Very Good - Clear word separation but underscores less visually distinct | Good - Word boundaries marked by capitals, but can be hard to distinguish in long names | Fair - Initial lowercase can blend words together |
| **Visual Clarity** | High - Hyphens create distinct separation | Medium-High - Underscores visible but less prominent | Medium - Capitals provide some distinction but no separators | Low - No separators and mixed case |
| **Name Length** | Shortest - Most compact format | Longest - Approximately 17% longer than kebab-case | Medium - No separators reduces length | Medium - No separators reduces length |
| **URL Compatibility** | Excellent - Native in URLs without encoding | Poor - Requires encoding in some contexts | Poor - Case often lost in URLs | Poor - Case often lost in URLs |
| **Shell Scripting** | Excellent - No escaping needed in most contexts | Good - May need escaping in some contexts | Poor - Requires quoting and careful handling | Poor - Requires quoting and careful handling |
| **Regex Pattern Matching** | Very Good - Simple patterns with escaped hyphens | Excellent - Underscores work well with word boundary matches | Fair - Requires complex patterns to match case boundaries | Fair - Requires complex patterns to match case boundaries |
| **SQL/Database Compatibility** | Fair - May conflict with SQL operators | Excellent - Standard in SQL identifiers | Fair - Often not supported in SQL | Fair - Often not supported in SQL |
| **Programming Language Standards** | JavaScript (files), CSS, HTML | Python, Ruby, SQL | C#, Java (classes), React Components | JavaScript (variables), Java (methods) |
| **Cross-Platform Filesystem Support** | Excellent - Works on all major systems | Excellent - Works on all major systems | Good - Case sensitivity issues on some systems | Good - Case sensitivity issues on some systems |
| **Sort Order Predictability** | Excellent - Alphabetical sorting works as expected | Excellent - Alphabetical sorting works as expected | Fair - Case-sensitive sorting may cause inconsistencies | Fair - Case-sensitive sorting may cause inconsistencies |
| **Search Engine Optimisation** | Excellent - Words properly separated in URLs | Good - Words not properly separated in URLs | Poor - Words not properly separated in URLs | Poor - Words not properly separated in URLs |
| **Cognitive Processing Speed** | Fast - 11% faster skimming than underscores | Medium - Less efficient visual processing | Slow - 19% more recognition errors in studies | Slow - Mixed case requires more cognitive effort |
| **AI/Automation Compatibility** | Excellent - Easy tokenisation and pattern matching | Very Good - Good tokenisation but more complex patterns | Fair - Requires specialised handling for case boundaries | Fair - Requires specialised handling for case boundaries |
| **Writing Speed** | Fast - Simple to type all lowercase with hyphens | Medium - Shift key required for underscores | Slow - Multiple shift keys required | Medium - Shifting between cases required |
| **Modern Framework Support** | High - Increasingly standard in modern tooling | Medium - Common in specific ecosystems | Medium - Reserved for specific use cases | Medium - Reserved for specific use cases |
| **Design Tool Compatibility** | Good - Works with most tools but not standard | Fair - Less common in design contexts | Excellent - Standard in Adobe and design tools | Good - Used in some design contexts |
| **Font Management Compatibility** | Poor - Conflicts with typography standards | Poor - Not used in font naming | Excellent - Industry standard for font families | Fair - Not typical for font naming |
| **Overall Recommendation for FOMO** | **Primary Standard** - Optimal for general files and contexts | Limited - Use primarily for Python files and SQL | Domain-Specific - Use for fonts, React components, and design tools | Not Recommended - Limited use cases within FOMO |

## Context-Specific Recommendations

### For General Files
Kebab-case provides the best balance of readability, compatibility, and automation support. It should be the default choice for most files in the system, including documentation, general assets, and configuration files.

### For Design Assets
Use a hybrid approach:
- Kebab-case for general design files and assets
- PascalCase for font files and families (following typography standards)
- Respect Adobe and design tool naming conventions where required

Design files benefit from clear state indicators and client identifiers, regardless of the case format chosen.

### For Development Files
While kebab-case is recommended as the default, follow established language and framework conventions:
- PascalCase for React components and class files
- snake_case for Python modules
- camelCase for JavaScript variables and methods
- Built-in framework conventions where established

### For Fonts and Typography
PascalCase is the industry standard for font family names and should be followed for all font files. The special notation for variable fonts with axis tags in square brackets must be respected for proper function.

### For Personal Files and Screenshots
Kebab-case offers the most intuitive format for personal organisation. Its easier typing (all lowercase with simple hyphens) makes it ideal for quick file creation and management of personal documents, screenshots, and notes.

### For System Integration
A layered approach provides the best outcomes:
- Level 1: Kebab-case for general system-wide files
- Level 2: Domain-specific formats where required by tools, standards, or frameworks

This balanced approach maintains system-wide consistency while respecting established industry practices in specialised domains.
