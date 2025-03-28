# File Naming Conventions: 2.  Standards & Approaches

---

# I. Standard Approach

Below is a detailed, step‐by‐step breakdown of a universal naming standard that **does NOT** use a date‐first approach. This structure is designed to integrate with your directory hierarchy and support version control practices.

---

## 1. Naming Structure Overview

**Naming Format:**

```
Project_Category_Description_Version[_YYYYMMDD].ext

```

*Note:* The optional date is placed at the end. This ensures that files are primarily grouped by project, aligning with your directory structure, while still offering a historical reference when needed.

---

## 2. Component Breakdown

The table below explains each component of the naming standard:

| **Component** | **Purpose** | **Example** | **Integration & Considerations** |
| --- | --- | --- | --- |
| **Project** | Identifies the associated project or client; aligns with the top-level directory. | `ClientA` or `MarketingCampaign` | Use a project name that mirrors your project folder (e.g. `/Projects/MarketingCampaign`). This grouping simplifies navigation and file retrieval. |
| **Category** | Denotes the file type or usage (e.g. document, image, code file). | `Doc`, `Img`, `Code` | Standardised codes ensure consistency. The category supports automated sorting and manual classification within your project directories. |
| **Description** | Provides a concise summary of the file’s content. | `ProjectProposal`, `LandingPage` | Keep the description brief (1–3 words) to enhance clarity. Use underscores to separate multiple words, which supports searchability and readability. |
| **Version** | Tracks file revisions for version control. | `v1`, `v2.1` | Increment the version number with each significant update. This component is critical for iterative design and development, and it works well alongside systems like Git. |
| **Optional Date** | Offers additional context regarding the creation or update date, placed after the version. | `20250206` | Including the date as an optional suffix provides historical context without disrupting the primary sorting by project. It should use the YYYYMMDD format. |
| **Extension** | Denotes the file format. | `.pdf`, `.jpg`, `.js` | The extension must match the file type; it is automatically recognised by the operating system and applications. |

---

## 3. Step-by-Step Example

Consider a code file within a marketing campaign project. The steps below illustrate how to build the file name:

1. **Project:**
    - Begin with the project name that matches the corresponding directory.
    - *Example:* `MarketingCampaign`
2. **Category:**
    - Add the code file category.
    - *Example:* `Code`
3. **Description:**
    - Provide a brief description of the file’s function.
    - *Example:* `LandingPage`
4. **Version:**
    - Append the version number to indicate the file iteration.
    - *Example:* `v2`
5. **Optional Date:**
    - Optionally add the date (YYYYMMDD) after the version for historical context.
    - *Example:* `20250206`
    - *If omitted, the file name will not include a date.*
6. **Extension:**
    - Conclude with the file extension.
    - *Example:* `.js`

**Resulting File Name (with date):**

```
MarketingCampaign_Code_LandingPage_v2_20250206.js

```

**Resulting File Name (without date):**

```
MarketingCampaign_Code_LandingPage_v2.js

```

---

## 4. Integration with Directory Hierarchy & Version Control

The following table explains how this naming standard supports your overall file management system:

| **Aspect** | **Integration Details** | **Key Benefits** |
| --- | --- | --- |
| **Directory Hierarchy** | The first element (Project) aligns directly with your top-level folders. For example, files stored in `/Projects/MarketingCampaign` begin with `MarketingCampaign`. | Simplifies navigation and maintains consistency across file systems. |
| **File Type Sorting** | The Category field (e.g. `Doc`, `Img`, `Code`) enables quick classification and automated sorting within each project folder. | Enhances searchability and supports tools like Hazel for automated sorting. |
| **Version Control** | The Version component (e.g. `v1`, `v2.1`) clearly identifies iterations of a file, aiding in tracking changes and coordinating updates within teams. | Facilitates easier tracking of revisions and is compatible with Git or similar systems. |
| **Optional Date** | Placing the date at the end provides additional context without affecting primary sorting by project or category. | Offers historical reference without disrupting the main hierarchy sorting. |

---

## 5. Final Considerations

- **Consistency:** Ensure that all team members use the same naming standard to maintain uniformity across projects.
- **Automation:** With a clear structure, automated tools can reliably parse each element for sorting, archiving, or version control purposes.
- **Documentation:** Create a style guide that details this naming convention. This document should be shared within your team for ongoing reference and training.

This detailed breakdown provides a comprehensive naming standard that avoids a date-first approach while integrating seamlessly with your directory hierarchy and version control practices. If you require further details on automating these conventions or additional file type codes, please let me know.

---

---

# II. Date-First Approach

Below is a detailed, step-by-step breakdown of the universal naming standard and how it integrates with your directory hierarchy. Each section is presented in a table format to ensure clarity.

---

### 1. Overall Naming Structure

| **Component** | **Purpose & Details** | **Example** | **Considerations** |
| --- | --- | --- | --- |
| Date | Provides chronological context; using ISO 8601 (YYYYMMDD) for uniformity and sorting. | `20250206` | Use for all files; optionally add time (e.g., `20250206_1530`) for time-sensitive files. |
| Project | Indicates the associated project or client; helps group files by context. | `ClientA` or `Internal` | Choose a clear project name; align with your directory project folders. |
| Category | Denotes the file type or usage; differentiates between documents, images, code files, etc. | `Doc`, `Img`, `Code` | Standardise codes across your team; consult the table below for common file type codes. |
| Description | Summarises file content succinctly; adds context beyond the file type and project. | `ProjectProposal` | Keep it brief (typically 1-3 words); avoid spaces and special characters (use underscores). |
| Version | Marks the file revision or iteration; supports version control within filenames. | `v1` or `v2.1` | Update consistently as files evolve; consider additional identifiers (e.g., beta, final) if needed. |
| Extension | The standard file format extension; identifies the file type to the operating system and applications. | `.pdf`, `.jpg`, `.js` | Do not modify manually; ensure file conversion or export tools use the correct extension. |

**Overall Naming Example:**

`20250206_ClientA_Doc_ProjectProposal_v1.pdf`

---

### 2. File Type Codes and Conventions

This table lists common file types and suggested codes to maintain consistency:

| **File Type** | **Code** | **Description** | **Example Filename Fragment** |
| --- | --- | --- | --- |
| Documents | Doc | Textual documents, reports, proposals | `Doc_ProjectProposal` |
| Images | Img | Photographs, designs, graphics | `Img_TeamPhoto` |
| Code Files | Code | Programming files, scripts, source code | `Code_LandingPage` |
| Spreadsheets | Sheet | Financial reports, data sheets | `Sheet_Budget2025` |
| Presentations | Pres | Slide decks and presentation files | `Pres_QuarterlyMeeting` |
| Videos | Vid | Recordings, screen captures, video content | `Vid_ProductDemo` |
| Audio | Aud | Podcasts, recorded meetings, voice files | `Aud_Interview` |
| Archives | Zip | Compressed files or project backups | `Zip_ProjectBackup` |

*Consider using these codes consistently to ensure files are easily identified by type within your hierarchy.*

---

### 3. Integrating with Your Directory Hierarchy

This section explains how the naming convention works in concert with your directory structure.

| **Aspect** | **Integration Details** | **Example** | **Notes** |
| --- | --- | --- | --- |
| Directory Hierarchy | Files are stored in project-specific or category-specific folders that mirror the naming convention components. | `/Projects/ClientA/Documents/` | Align the project and category fields in your filenames with the folder names. |
| Automated Sorting | Tools such as Hazel or custom scripts can parse the naming components to move files into the correct folders automatically. | Hazel rule parsing on `_*_Doc_*` | Ensure the naming structure is consistent to allow reliable automation. |
| Searchability | A clear naming format improves retrieval via Spotlight, Finder, or other search utilities by filtering date, project, or type. | Search for `20250206_ClientA` | Consider adding metadata or tags if further sorting is needed. |
| Version Control | File versioning in the name simplifies tracking iterations and changes over time. | Update to `v2.1` as the file evolves | Consider integration with version control systems for code files if required. |

---

### 4. Detailed Walkthrough Example for a Code File

Let’s work through an example of naming a code file that belongs to a project:

| **Step** | **Explanation** | **Applied Example** |
| --- | --- | --- |
| **1. Date** | Record the creation or significant update date in YYYYMMDD format. | `20250206` |
| **2. Project** | Indicate the project name or client associated with the code file. | `MarketingCampaign` |
| **3. Category** | Use the file type code for code files. | `Code` |
| **4. Description** | Briefly describe the function or component of the code. | `LandingPage` |
| **5. Version** | Specify the version of the code file. | `v2` |
| **6. Extension** | Use the appropriate extension for the code language. | `.js` |

**Final File Name:**

`20250206_MarketingCampaign_Code_LandingPage_v2.js`

---

### 5. Implementation Considerations

| **Consideration** | **Detail** | **Action** |
| --- | --- | --- |
| Consistency | Ensure every team member follows the same naming rules to maintain uniformity. | Develop and distribute a style guide for file naming. |
| Automation Compatibility | The structure should allow automation tools to reliably extract components (e.g., date, project, category) for sorting. | Test naming convention with your automation tool (e.g., Hazel rules). |
| Adaptability | The naming standard should be flexible enough to adapt to additional file types or changes in project structure over time. | Regularly review and adjust the naming standard as the project or tool evolves. |
| Documentation | Maintain a central reference document that explains each component and example for future reference. | Create a style guide and circulate within the team. |

---

### Final Thoughts

This detailed breakdown addresses each component of the universal naming standard one step at a time, ensuring integration with your directory hierarchy. Consistency and clear documentation are key to maximising the benefits of this approach, from manual file management to automated sorting.

Do you need further assistance with setting up automated sorting rules or additional file type conventions?