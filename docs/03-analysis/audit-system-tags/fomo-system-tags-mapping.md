### **1. Mapping Current Tag Categories to FOMO Tags**

Final tags:
`#todo` - tag colour `red`
`reference` - tag colour `yellow`
`#archive` - tag colour `grey`
`#work` - tag colour `orange`
`#personal` - tag colour `green`
`#family` - tag colour `blue`

---

Use Comments, metadata, file extensions, etc instead tags. Combiend with smart folder searches, e.g.:
`Keywords: web app, ai` (always lower case, separated by comma)
`Category_HEAD: design` 

---


**10x Category & Index tags (not system tags)**
- .dir: 6 files       -> ~~removed~~
- .lib: 1+1 files     -> ~~removed~~
- -system: 3 files    -> #admin?? TBC

- -personal: 8 files  -> #personal
- -family: 7 files    -> #family
- -media: 8 files     -> #personal
- -finance: 7 files   -> #family

- -project: 5 files   -> #todo?? TBC
- -work: 6 files      -> #work
- -design: 4 files    -> #work


**8x Status/Workflow tags (prefixed with =):**
- =archive: 100 files   -> #archive
- =working: 37 files    -> ??remove?? 
- =final: 22 files      -> ??remove??  
- =portfolio: 18 files  -> #reference or #work
- =folio: 38 files      -> #reference or #work
- =template: 6 files    -> #??remove?? use [TPL] in folder/file name?
- =reference: 164 files -> #reference
- =asset: 38 files      -> #reference or #work or [AST] in folder name?


**7x Other tag: Colour & Special**
- Sort: 67 files             -> #todo
- Flag: 1525 files           -> #reference, needs review
- Yellow: 185 files = FLAG   -> #reference, needs review
- Green: 10 files = WORKING  -> ??remove??
- Blue: 1 file = FINAL       -> ??remove??


**10,000x PostScript-type1:** 
- 58754 files (largest group)  -> Use FiletTyle instead


**11x Media realted, Resolution & Duration tags**
- 1080p: 89 files     -> Use Metadata instead
- 720p: 164 files
- 480p: 500 files
- 1440p: 1 file
- 2160p: 2 files
- dur-0: 47 files     -> Use Metadata instead
- dur-5: 103 files
- dur-10: 284 files
- dur-30: 112 files
- tvShow: 43 files
- xxx: 2 files



Solutions:
Use comments, metatdata or file extensions, etc instead tags. Combiend with smart fodler seraches
- Comments: Use comments to store detailed information about files, such as resolution, duration, or special notes. This keeps the tags list clean while providing necessary context.
- Metadata: Leverage file metadata to store resolution, duration, and other technical details. This way, you can search for files based on these attributes without cluttering your tag list.
- File Extensions: Use file extensions or naming conventions to indicate resolution or other technical specifications. For example, you could name files with resolution details like "filename_1080p" or "filename_720p" for easy identification.









#### Option 1: Minimalist FOMO (Core-Only Approach)

*This option uses only the core FOMO tags and offloads finer details to file metadata or supplementary systems.*

- **Resolution Tags (1080p, 720p, etc.)**
  • **Mapping:** Remove from core tags; record as file metadata or within filenames if resolution is crucial.
  • **Pros:** Simplifies tagging; reduces tag clutter.
  • **Cons:** Loss of immediately visible resolution info.

- **Status/Workflow Tags (e.g. =working, =archive, =final, =template, etc.)**
  • **Mapping:**
    - `=archive` → **#archive**
    - `=reference` → **#reference**
    - Others like `=working`, `=final`, `=template`, `=asset`, `=portfolio` can be maintained in a separate status field or noted in the file description.
  • **Pros:** Core statuses align with FOMO; extra statuses are handled elsewhere.
  • **Cons:** Requires supplementary tracking for detailed workflow stages.

- **Category Tags (e.g. -family, -work, -personal, -media, -project, -finance, -system, -design)**
  • **Mapping:**
    - `-family` → **#family**
    - `-work** and **-project** → **#work**
    - `-personal** and **-finance** → **#personal**
    - `-media, -system, -design` → Reassign based on context (e.g. if work-related, then **#work**; if reference material, then **#reference**).
  • **Pros:** Direct mapping of key areas; keeps the main splits clear.
  • **Cons:** Some nuance may be lost if you need a finer-grained distinction.

- **Duration Tags (dur-0, dur-5, dur-10, dur-30)**
  • **Mapping:** Use as file attributes rather than tags.
  • **Pros:** Keeps file attributes without cluttering the tag list.
  • **Cons:** Requires reliance on metadata search instead of tag search.

- **Color Tags (Green, Blue, Yellow)**
  • **Mapping:** Replace with native colour labels (e.g. in Finder) to maintain visual cues.
  • **Pros:** Utilises built-in visual organisation features.
  • **Cons:** Might require a change in workflow if you’re used to custom tags.

- **Special Tags (Flag, Sort, PostScript-type1, tvShow)**
  • **Mapping:**
    - **Flag:** Could remain as an indicator (or be replaced by the system’s flagging feature).
    - **Sort:** May be dropped or integrated into file naming conventions.
    - **PostScript-type1 and tvShow:** Reassign based on context (e.g. tvShow might fall under **#personal** or **#reference**).
  • **Pros:** Simplifies special cases.
  • **Cons:** You lose some specialised descriptors unless recorded elsewhere.

- **System Tags (.dir, .lib)**
  • **Mapping:** Remove these from the tagging system; use them as part of your file system structure only.
  • **Pros:** Avoids cluttering the tagging schema with internal management markers.
  • **Cons:** None—their function is already separate from file categorisation.

---

#### Option 2: Layered FOMO (Core Plus Sub-Categorisation)

*This option preserves more of your current distinctions by retaining the FOMO core while appending sub-tags or metadata fields for additional detail.*

- **Resolution Tags:**
  • **Mapping:** Create a sub-field or use a suffix (e.g. `#work_1080p`) when resolution is essential. Alternatively, store in metadata.
  • **✓ Strength:** Retains resolution detail visibly.
  • **✗ Limitation:** Increases tag variations slightly.

- **Status/Workflow Tags:**
  • **Mapping:**
    - `=archive` → **#archive**
    - `=reference` → **#reference**
    - Other statuses can be appended as secondary tags (e.g. `#work_working` or `#personal_final`).
  • **✓ Strength:** Keeps a quick reference to file status.
  • **✗ Limitation:** May introduce more tags; however, you can limit these to active projects.

- **Category Tags:**
  • **Mapping:**
    - Directly map `-family` to **#family**, `-work` to **#work**, `-personal` to **#personal**.
    - For tags like `-media, -project, -finance, -system, -design`, use additional sub-tagging or metadata fields (e.g. `#work_media` or a custom metadata field labelled “Category”).
  • **✓ Strength:** Preserves nuanced distinctions.
  • **✗ Limitation:** Requires disciplined use of sub-tags or metadata.

- **Duration, Colour, and Special Tags:**
  • **Mapping:** Integrate as custom metadata fields that are searchable, or use a suffix approach (e.g. `#todo_dur10` or `#reference_Blue`) if the distinction is critical.
  • **✓ Strength:** Detailed searchability remains.
  • **✗ Limitation:** Increases the learning curve and requires a consistent naming convention.

- **System Tags:**
  • **Mapping:** As with Option 1, remove these from the tagging system.
  • **Pros/Cons:** Same as above.

---

### **2. Step-by-Step Plan for Implementing the Tag Consolidation**

1. **Audit & Backup**
   • **Inventory:** Create a complete list or spreadsheet of your current tags, categorising them as shown above.
   • **Backup:** Export current tagging data (if possible) so you can revert if needed.

2. **Define Your Core Mapping**
   • Decide between Option 1 (Minimalist) or Option 2 (Layered).
   • Document your mapping rules clearly.
   • Example mapping table:

   | Current Tag Category        | Example Tags                     | Minimalist Mapping                   | Layered Mapping                           |
   |-----------------------------|----------------------------------|--------------------------------------|-------------------------------------------|
   | Resolution                  | 1080p, 720p                      | Move to metadata                     | Append suffix or use metadata             |
   | Status/Workflow             | =working, =archive, =final       | =archive → **#archive**, others in notes | =archive → **#archive**; others as `#work_working` etc. |
   | Category                    | -family, -work, -media           | -family → **#family**; -work → **#work**; others as context-specific | Same as Minimalist, with optional sub-tags |
   | Duration                    | dur-0, dur-5                     | Move to metadata                     | As metadata or appended (if critical)      |
   | Colour                      | Green, Blue, Yellow              | Use native colour labels             | Same as Minimalist                         |
   | Special                     | Flag, Sort, tvShow               | Retain Flag as native flag; drop Sort; reassign tvShow | Use as sub-tags if necessary              |
   | System                      | .dir, .lib                       | Remove from tag system               | Remove from tag system                     |

3. **Pilot Testing**
   • Select a subset of frequently used files.
   • Apply your new FOMO tags manually based on your mapping.
   • Test Smart Folder setups (e.g. in Finder or Notes) to verify that files are being grouped correctly.

4. **Automate with Tools**
   • For **Finder:** Set up Smart Folders for each FOMO tag. Use Hazel or Shortcuts to auto-assign tags based on file location or name patterns.
   • For **Notes/Reminders:** Create Smart Folders and automate tagging using Apple Shortcuts where possible.

5. **Gradual Rollout & Cleanup**
   • Begin tagging new files exclusively with the FOMO system.
   • Periodically review older files; consider a “review folder” to batch-update tags.
   • Monitor automation rules and adjust based on any workflow issues.

6. **Documentation & Consistency**
   • Keep a brief guide (or cheat sheet) of your mapping rules visible until you’re comfortable with the new system.
   • Schedule a monthly review to ensure consistency and to consolidate any tags that might still be redundant.

---

### **Summary Comparison**

| Option                   | Strengths                                   | Limitations                                 | Best For...                                |
|--------------------------|---------------------------------------------|---------------------------------------------|--------------------------------------------|
| **Minimalist FOMO**      | ✓ Streamlined, easy to maintain             | ✗ Some fine details (e.g. resolution, status) are relegated to metadata | Users seeking a clean, minimal system      |
| **Layered FOMO**         | ✓ Preserves key nuances with sub-tags/metadata | ✗ Slightly more complex and requires disciplined naming | Users needing visible fine-grained distinctions |

---

By adopting one of these approaches, you’ll reduce your tag list significantly while still preserving the essential distinctions for effective file organisation. For more details on the FOMO system principles and implementation ideas, see the FOMO Unified Tagging System documentation citeturn0file0.

*[High Confidence]*
