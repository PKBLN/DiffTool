# DiffTool
File comparison tool in just one HTML file

An in-browser tool to compare ZIP archives or plain text files side by side with line-level diffs. Supports drag & drop and is available in German and English.

<img width="1914" height="1219" alt="grafik" src="https://github.com/user-attachments/assets/d66f1ae8-154d-4177-bf52-c945f67de7a1" />
<img width="1849" height="1146" alt="grafik" src="https://github.com/user-attachments/assets/cfb96448-e7a4-4636-8f05-201eeba89195" />


## Features

- Compare two ZIP files (content-aware) or two text files
- Compare a ZIP file against a single text file (matches by filename)
- Fast mode: file-level comparison for ZIPs via hashing (no line diffs)
- Regex line filter: ignore lines matching a user-provided regular expression
- Adjustable diff context (lines before/after changes)
- Drag & drop anywhere on the page with automatic assignment to Reference and Comparison
- Multilingual UI (Deutsch/English) with a language selector and persistence
- Client-side only, no uploads, powered by JSZip

## Getting Started

1. Open the HTML file in a modern browser:
   - zip_diff_tool_DE.html
2. Choose your language using the dropdown in the header (persisted between sessions).
3. Select or drag & drop your files:
   - First panel: reference file
   - Second panel: comparison file
   - You can drop one or two files anywhere on the page; the first two will be auto-assigned.
4. Optional settings:
   - Fast mode (ZIP only): show file-level differences only
   - Regex filter: lines matching the pattern will be ignored before diffing
   - Context lines: adjust how many surrounding lines are shown around changes
5. Click “Compare →” to start the comparison.

## Drag & Drop

- A global drop zone activates when dragging files over the page.
- Drop one file: it fills the first empty slot; if both are filled, it replaces the reference file.
- Drop two or more files: the first two files are assigned to reference and comparison.

## Languages

- The interface supports German (de) and English (en).
- Use the dropdown in the header to switch; your choice is saved in localStorage.

## Privacy

- All processing happens in your browser. Files are not uploaded anywhere.

## Credits

- JSZip: https://stuk.github.io/jszip/

## Development Notes

- A lightweight i18n dictionary is embedded in the HTML. Add new keys by:
  - Marking texts with `data-i18n="your_key"` and
  - Providing translations under `translations.de` and `translations.en` in the script.
- The previous debug UI has been removed to simplify the interface.
