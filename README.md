# AutoHotkey CSS Media Queries Script

## Overview

This AutoHotkey (AHK) script is designed to insert a series of CSS media queries into your text editor or IDE with a single key press. When you press the F8 key, the script sends four different media queries for various viewport widths, with each query separated by a blank line. After sending the queries, it performs some cleanup actions to ensure the text is formatted correctly.

## Features

- Sends media queries for different viewport widths.
- Waits between sending each query to ensure proper insertion.
- Cleans up extra characters after inserting the queries.

## Script Details

### Key Binding

- **F8**: Triggers the insertion of media queries.

### Media Queries

The script inserts the following CSS media queries:

```css
@media (max-width: 1200px) {
  /* Blank line */
}
/* Blank line */
@media (max-width: 768px) {
  /* Blank line */
}
/* Blank line */
@media (max-width: 480px) {
  /* Blank line */
}
/* Blank line */
@media (max-width: 220px) {
  /* Blank line */
}
```
## Script Actions

1. **Inserting Media Queries**:
   - The script sends a series of CSS media queries, each followed by a newline.
   - The media queries are for different viewport widths, specifically:
     - `@media (max-width: 1200px) {}` 
     - `@media (max-width: 768px) {}` 
     - `@media (max-width: 480px) {}` 
     - `@media (max-width: 220px) {}`

2. **Sleep Intervals**:
   - The `Sleep` commands introduce delays between sending each media query and after the queries to ensure that the text editor processes the input correctly.
   - The script waits:
     - 100 milliseconds between each media query.
     - 900 milliseconds after sending all queries.
     - 1200 milliseconds before performing cleanup actions.

3. **Cleanup**:
   - **Delete**: Removes the last 8 characters from the inserted text.
   - **Backspace**: Deletes 2 additional characters to adjust formatting.

These actions ensure that the media queries are correctly inserted and formatted in your document.


### 2. Configuring the Script to Start Automatically

To ensure that your AutoHotkey script runs automatically every time you start your computer:

1. **Create the Script as Described Above:**
   - Follow the instructions in the previous section to create your AutoHotkey script.

2. **Add the Script to the Startup Folder:**
   - Press **Win + R** to open the **Run** dialog.
   - Type `shell:startup` and press **Enter**. This opens the **Startup** folder.
   - Copy your script file (e.g., `MyScript.ahk`) into this folder.

After completing these steps, your script will automatically run every time you start your computer, ensuring that your custom shortcuts are always available.

