# Instant Data Scraper
## Chrome Extension

## Bugs
- The original extension is working fine, but suddenly this (unpacked) extension stopped working!!
    - Error message (in JS Console) : `Unchecked runtime.lastError: Could not establish connection. Receiving end does not exist.`

### Feature Request by Anil Sir
Add CSV Column Mapping:
    - **Why:** The default CSV generated has random column headings based on source HTML.
    - When first running Instant Data Scraper for a type of URL, give an option to generate a **Mapping File**.
        - The Mapping File will map generated column names to required column names.
        - Columns not required will be dropped.
    - On next run, give an option to see *Mapped CSV* and download that instead of original CSV.

### How to do this Mapping
1. Enable Developer Mode for Chrome Extensions.
2. Install from disk instead of pre-packaged extension.
3. Inspect and find where CSV is generated.
4. How to modify CSV (any package required) ?
5. Add button, or else toggle mode for Mapped CSV instead of original CSV (using fixed mapping).
6. Now add option for generating Mapping on first run.

### PROBLEMS
- Which URLs are "similar" ?
- Where should mapping be stored (maybe in $HOME) ?
- What format should mapping be stored in (maybe CSV) ?
- How will the whole "Auto Generating Mapping" interface work?
    - Maybe allow renaming / leaving blank (or deleting) column names from generated CSV?
    - or maybe delegate to another program like Excel?

### NOTES
- In *popup.js*:
    - CSV Data stored in `generatedCSVData` variable on line 205. (**Note:** I have made it a global variable now.)
    - `tableData` global variable holds all data about currently selected table, user modifications, etc.

