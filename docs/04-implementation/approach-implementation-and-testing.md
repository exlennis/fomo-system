## Implementation and Testing Approach

### Phase 1: Initial Setup and Quick Testing

1. **Create a Test Directory Structure**
	- Set up a parallel directory structure that mirrors your actual working environment
	- Include sample files of different types (documents, images, code files)
	- Use this area for testing without disrupting your current workflow
		
2. **Develop Basic Automation Tools**
	- **Hazel Rule for Screenshots**: Create a rule that automatically renames screenshots using the new pattern
	- **Shortcut for Document Saving**: Create an Apple Shortcut that helps format document names during save operations
	- **Simple Python Script**: Develop a basic script for batch renaming existing files
		
3. **Manual Testing Process**
	- Create a small test set of 20-30 files across different categories
	- Apply naming conventions manually to feel out any awkward patterns
	- Note any difficulties or inconsistencies encountered

### Phase 2: Focused Real-World Testing
	
1. **Apply to New Files Only**
	- Start using the conventions for all new files you create
	- Keep a journal noting any challenges or instances where the conventions feel restrictive
	- Track the time spent thinking about naming versus your previous approach
	
2. **Refine Automation Tools**
	- Adjust rules based on initial findings
	- Create more sophisticated shortcuts for common file types
	- Develop scripts to validate naming compliance
	
3. **Test Searchability and Sorting**
	- Practice searching for files using the new naming patterns
	- Evaluate how well files sort in file explorers and search results
	- Compare retrieval time with your previous system

### Sample Automation Rules and Scripts

#### 1. Hazel Rule for Screenshots

```
Rule: "Screenshot Auto-Naming"
Condition: Filename extension is "png" or "jpg" AND Filename contains "Screen Shot" or "Screenshot"
Actions:
1. Rename with pattern: "screenshot-{app}-{date}-{time}.{extension}"
   - {app}: Get from foreground application at time of capture (if available) or "unknown"
   - {date}: Format as YYYYMMDD
   - {time}: Format as HHMMSS
2. Move to Screenshots folder within project directory
```

#### 2. Python Script for Batch Renaming

Automated Renaming Script Example:

```python
import os
import re

def normalize_filename(filename):
    # Convert spaces and underscores to hyphens
    normalized = re.sub(r'[\s_]+', '-', filename.lower())
    # Remove special characters
    normalized = re.sub(r'[^\w\-\.]', '', normalized)
    return normalized

def rename_files(directory):
    for root, dirs, files in os.walk(directory):
        # Rename directories
        for dir_name in dirs:
            new_name = normalize_filename(dir_name)
            if dir_name != new_name:
                os.rename(
                    os.path.join(root, dir_name),
                    os.path.join(root, new_name)
                )
        
        # Rename files
        for filename in files:
            new_name = normalize_filename(filename)
            if filename != new_name:
                os.rename(
                    os.path.join(root, filename),
                    os.path.join(root, new_name)
                )
```

Here's a Python script that could test rename operations on a batch of files:

```python
import os
import re
import datetime

def rename_files_in_dir(directory):
    """Rename files in directory according to FOMO naming standards."""
    for filename in os.listdir(directory):
        # Skip directories and hidden files
        if os.path.isdir(os.path.join(directory, filename)) or filename.startswith('.'):
            continue
            
        # Get file extension
        name, ext = os.path.splitext(filename)
        ext = ext.lower()  # Lowercase extension
        
        # Example: Convert to kebab-case
        new_name = name.lower()
        # Replace spaces and underscores with hyphens
        new_name = re.sub(r'[\s_]+', '-', new_name)
        # Remove special characters
        new_name = re.sub(r'[^\w\-\.]', '', new_name)
        # Replace multiple hyphens with single hyphen
        new_name = re.sub(r'-+', '-', new_name)
        
        # Add date if not present (example only - real implementation would be more nuanced)
        if not re.search(r'\d{8}', new_name):
            today = datetime.datetime.now().strftime('%Y%m%d')
            new_name = f"{new_name}-{today}"
            
        # Add version if not present
        if not re.search(r'v\d{2}', new_name):
            new_name = f"{new_name}-v01"
            
        # Combine with extension
        new_filename = f"{new_name}{ext}"
        
        # Rename the file
        if filename != new_filename:
            print(f"Renaming: {filename} → {new_filename}")
            os.rename(
                os.path.join(directory, filename),
                os.path.join(directory, new_filename)
            )

# Example usage
# rename_files_in_dir('/path/to/test/directory')
```

#### 3. Apple Shortcut for Document Naming

Create a Shortcut with these steps:
1. Ask for input: "Project Name" (text)
2. Ask for input: "Document Type" (with predefined options like report, proposal, notes)
3. Ask for input: "Description" (text)
4. Get current date (formatted as YYYYMMDD)
5. Combine text: [Project]-[Type]-[Description]-[Date]-v01
6. Copy to clipboard or use in Save dialog

### Feedback Collection System

To systematically gather insights during testing:

1. **Create a Simple Evaluation Form**
	- Rate the naming convention's clarity (1-5)
	- Note time spent deciding on a filename (seconds)
	- Document any situations where the conventions felt limiting
	- Record any suggested improvements
	
2. **Track Metrics**
	- Time spent finding specific files
	- Number of times you needed to open a file to identify it
	- Instances where automation correctly/incorrectly applied naming
	
3. **Regular Review Sessions**
	- Schedule a weekly 15-minute session to review your findings
	- Update the naming standards document with insights
	- Adjust automation rules based on real-world usage

## Conclusion

The FOMO Naming Standards document provides an excellent foundation, and your suggested improvements will make it even more practical. By adding an overarching component order framework and simplifying the screenshot template, the document will better guide users through the decision-making process.

The key to success will be thoughtful implementation and systematic testing in real-world scenarios. The automation suggestions provided should help you quickly test the conventions with minimal disruption to your workflow.

Remember that this is an iterative process. As you use these conventions in practice, you'll likely discover additional refinements that make the system even more effective. The goal is to develop standards that feel intuitive and reduce cognitive load rather than adding complexity.

Would you like me to help you implement any of these suggested changes directly to your FOMO Naming Standards document? Or would you prefer more detailed examples of any particular automation approach?


---


## Tools & Configurations

### 1. Git Hooks (pre-commit)

```bash
#!/bin/bash
# .git/hooks/pre-commit

# Check file naming conventions
files=$(git diff --cached --name-only --diff-filter=ACM)
invalid_names=$(echo "$files" | grep -E '[A-Z]|[[:space:]]|\+|&|@|\$|%|\^')

if [ ! -z "$invalid_names" ]; then
    echo "Error: Invalid file names found:"
    echo "$invalid_names"
    exit 1
fi
```


### 2. ESLint Configuration

```json
{
  "rules": {
    "filename-naming-convention": [
      "error",
      {
        "directories": "kebab-case",
        "extensions": ["js", "ts", "tsx"],
        "ignore": ["README.md", "LICENSE"]
      }
    ]
  }
}
```


### 3. VS Code Settings

```json
{
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "files.exclude": {
    "**/*.bad-extension": true
  }
}
```





## CI/CD Integration

### GitHub Actions Example

```yaml
name: Naming Convention Check

on: [push, pull_request]

jobs:
  check-names:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      
      - name: Check File Names
        run: |
          find . -type f -name "*[A-Z]*" -o -name "* *" \
            -o -name "*[+&@$%^]*" > invalid_files.txt
          
          if [ -s invalid_files.txt ]; then
            echo "Invalid file names found:"
            cat invalid_files.txt
            exit 1
          fi
```

### Compliance Checks Custom Script Example

```bash
find . -name "*[A-Z]*" -o -name "* *" -o -name "*[\!@#\$]*"
```
 

### Edge Case Decision Matrix Example

| Scenario | Convention | Rationale |
| :-- | :-- | :-- |
| Mixed-language documents | `report-en-fr-v1.md` | Language codes for clarity |
| Confidential files | `CONFIDENTIAL-` prefix | Immediate visual warning |
| Temporary files | `tmp-` prefix + date | Easy bulk deletion |


## Implementation Workflow

1. **Initial Setup**
    - Install linting tools and git hooks
    - Configure IDE settings
    - Set up automated naming validations (CI/CD/Git checks)
    - Standardise acronyms (e.g., `design`, `dev`)
2. **Onboarding**
    - Review naming conventions in team meeting
    - Add conventions to development guidelines (`/docs/standards/NAMING_CONVENTIONS.md`)
    - Create template with naming checklist
3. **Maintenance**
    - Regular automated audits
    - Maintain log for edge cases
    - Update conventions as needed
    - Review and refine automation rules
4. **Migration Strategy**
    - Run rename script on legacy files
    - Update documentation references
    - Test system after mass renaming
    - Create backup before migration

## Additional Tools

- [rename-cli](https://github.com/jhotmann/node-rename-cli): CLI tool for batch renaming
- [prettier](https://prettier.io/): Code formatting including file names
- [husky](https://typicode.github.io/husky/): Git hooks made easy
- [lint-staged](https://github.com/okonet/lint-staged): Run linters on staged files

Remember to adapt these tools and rules to your specific project needs while maintaining consistency with the established conventions.




---

### Batch Processing Efficiency

Hyphenated names reduce 14% of escaping overhead in shell scripts according to Linux Foundation metrics. Example:

	
	```bash
	# Hyphen advantage
	for file in project-*.log; do
	  process "$file"
	done
	
	# Underscore requires quoting
	for file in "project_*.log"; do
	  process "$file"
	done
	```


### Automation for Renaming

Screenshots Hazel (Recommended)

	```
	Create a rule to match Screen Shot* files.
	Use a custom renaming format:
	
	screenshot_%custom_text%_%date_created:YYYYMMDD-HHMMSS%.png
	Extract app name from metadata (if possible).
	```
	
Apple Shortcuts
Run a shortcut to rename new screenshots automatically.
Terminal Command (Batch Rename)
Run this command in Terminal to rename all screenshots in your folder:

	
```
	for file in ~/Desktop/*.png; do
	  timestamp=$(stat -f "%Sm" -t "%Y%m%d-%H%M%S" "$file")
	  mv "$file" "screenshot_macbook_unknown_${timestamp}.png"
	done
```