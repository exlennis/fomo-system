# FOMO Maintenance Log v01

*A simple record of what I tried, what worked, what broke, and what I learned along the way.*

## About This Log

### Why Keep This Log
This is my personal breadcrumb trail so I can:
- Remember how I fixed that weird file naming issue 6 months ago
- Avoid repeating mistakes I've already made
- Track which parts of my system are actually making life easier
- Remember the "why" behind my decisions when I revisit this later

### How To Use It
- **Keep it casual**: Just jot down notes when something interesting happens
- **Delegate when possible**: Let Claude or other AI assistants update it
- **Newest stuff first**: Latest entries at the top so they're easy to find
- **Focus on the useful bits**: Only record what future-me would want to know

## Log Entries

### 2025-03-28: Fixed Symlink Establishment Issue

#### What I Did Today
- Updated section 7.3 in the directory structure guidelines (v03)
- Added proper verification steps before creating symlinks
- Created a script to automatically backup existing directories before symlinking
- Added a clear warning note about symlink behaviour with existing directories

#### What Broke
- Discovered that symlinks were being created *inside* existing directories instead of replacing them
- This caused unexpected nested symlinks that broke the directory structure
- The original guidelines didn't account for pre-existing directories like ~/Downloads

#### How I Fixed It
- Added a loop to check for and backup existing directories before creating symlinks
- Created a more informative warning about symlink behaviour
- Structured the implementation into clear, separate steps

#### Random Thoughts
- This is a common stumbling point when implementing symlink-based structures
- The updated guidelines make the system more robust for first-time setup
- Should consider adding this kind of verification to all filesystem operations

---

### 2025-03-03: First Day Testing

#### What I Did Today
- Set up a test folder with the new kebab-case naming
- Created my first Hazel rule for screenshots
- Tried renaming about 20 random files to see how it feels

#### What Broke
- The screenshot Hazel rule choked on emoji in filenames
- Found it awkward to remember the exact order of date-project-version

#### How I Fixed It
- Added a step in Hazel to strip emojis before processing
- Made a cheat sheet for naming patterns and stuck it on my desktop

#### Random Thoughts
- The kebab-case actually looks nicer than I expected
- Automation feels worth it for screenshots since I take so many
- Still not sure about the right approach for client files - need to think about it

---

### YYYY-MM-DD: Template for Future Entries

#### What I Did 
- Changes I made to my system
- New automation I set up
- Areas I organised

#### What Broke
- Problems I ran into
- Things that didn't work as expected
- Annoying issues worth remembering

#### How I Fixed It
- Solutions that worked
- Workarounds I discovered
- Things I'm still figuring out

#### Random Thoughts
- Stuff that's working surprisingly well
- Ideas for future improvements
- Notes to my future self

---

## Regular Check-ins

### March 2025

#### What's Working Well
- Parts of the system I'm happy with
- Time-saving tricks discovered
- Example: *"Screenshot automation is actually saving me time"*

#### Pain Points
- Things that are still frustrating
- Bottlenecks in my workflow
- Example: *"Still spending too much time sorting downloads"*

#### Ideas to Try
- New approaches I want to experiment with
- Simple improvements to implement
- Example: *"Try using Hazel to auto-sort PDFs based on content"*

#### System Tweaks Made
- Changes to my original plan based on actual usage
- New shortcuts or rules created
- Example: *"Added a quick screenshot renaming shortcut to Touch Bar"*

---

## Notes for AI Helpers

Hey AI assistants (especially future Claude):

You can help maintain this log after we've worked on the FOMO system. Just add new entries at the top following the template. Keep it casual but useful - imagine you're leaving notes for me to find later when I inevitably forget how I solved a problem.

Some examples of when to update this log:
- After we've set up a new automation
- When we discover and fix a weird edge case
- If we change our approach to something
- When I mention something is working really well or poorly

Sample prompt I might use: "Hey Claude, can you add today's screenshot automation fixes to the maintenance log? Especially that trick we figured out for handling spaces in filenames."

---

*Version History:*
- v01 - 2025-03-03: Initial log structure created
