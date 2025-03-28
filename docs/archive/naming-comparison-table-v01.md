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
| **Overall Recommendation for FOMO** | **Primary Standard** - Optimal for most files and contexts | Secondary - Use for Python files and SQL | Limited - Use only for React components and class files | Not Recommended - Limited use cases within FOMO |

## Context-Specific Recommendations

### For Design Assets
Kebab-case provides the clearest visual distinction between words and works seamlessly with design automation tools. The enhanced readability speeds up asset management and reduces errors when working with large asset libraries.

### For Development Files
While kebab-case is recommended as the default, allow for:
- PascalCase for React components
- snake_case for Python modules
- Built-in framework conventions where established 

### For Personal Files and Screenshots
Kebab-case offers the most intuitive format for personal organisation. Its easier typing (all lowercase with simple hyphens) makes it ideal for quick file creation and management of personal documents, screenshots, and notes.

### For System Integration
Kebab-case provides the best cross-platform compatibility, especially for files that may need to be shared via URLs, used in command-line operations, or processed by automation tools across different operating systems.
