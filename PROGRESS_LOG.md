# Prompt Sanitizer/Desanitizer - Progress Log
Generated: 2025-12-22

## Application Overview
A localized web application that helps users sanitize/desanitize sensitive information before plugging it into AI tools. The app provides a secure way to replace sensitive data with placeholder references and reverse the process when needed.

## Current Features

### Core Functionality
1. **Sanitize**: Replace sensitive information with placeholder references (e.g., {ref 1}, {ref 2})
2. **Desanitize**: Restore original text from sanitized placeholders
3. **Copy Output**: Copy sanitized/desanitized text to clipboard
4. **Clear All**: Reset input and output fields

### Mapping Management
1. **Mapping Sets**: Create and manage multiple reusable mapping sets
   - Create new mapping sets with custom names
   - Switch between different mapping sets
   - Delete mapping sets
   - View mapping count for each set

2. **Mapping Editor**:
   - Add new mappings (button positioned at top of list)
   - New mappings appear at the top of the list
   - Auto-generated replacement values: {ref N} where N increments
   - Edit mappings inline with two-column layout (Original → Replacement)
   - Remove individual mappings
   - Collapsable mappings section with smooth animation

3. **CSV Import**: Upload CSV files to bulk import mappings
   - Supports optional header row
   - Two-column format: Original, Replacement
   - Handles quoted values and escaped characters

### Advanced Features
1. **Case Insensitive Matching**: Mappings match regardless of case
   - "ABC" will match "abc", "Abc", "ABC", etc.

2. **Overlapping Pattern Handling**: Intelligent processing of nested patterns
   - Sorts mappings by length (longest first)
   - Prevents partial replacements (e.g., "ABC-123" won't become "{ref1}-123")

3. **Wildcard Options**:
   - All Emails: Automatically detect and replace email addresses with [email]
   - All Phone Numbers: Detect US phone number formats and replace with [phone]

4. **Highlighting System**:
   - Visual feedback showing what text was replaced
   - Highlights appear in both input and output displays
   - Configurable highlighting: "Highlight" checkbox toggles persistent highlighting
   - Persistent mode: highlights remain visible
   - Non-persistent mode: highlights fade out after 2 seconds

5. **Resizable Text Containers**:
   - Both input and output boxes support vertical and horizontal resizing
   - Resize handles on bottom-right corner
   - Maintains proper scrolling for overflow content

### Data Persistence
- All settings and mappings saved to browser localStorage
- Persisted data includes:
  - Mapping sets and their mappings
  - Currently selected mapping set
  - Wildcard settings (emails, phones)
  - Mappings collapsed state
  - Highlight persistence setting

### UI/UX Features
1. **Two-Panel Layout**:
   - Left sidebar: Mapping management and configuration
   - Right panel: Text input/output and controls

2. **Color Palette**: Experient brand colors
   - Primary: #71a9bf (blue gradient)
   - Secondary: #597e93
   - Accent: #92bdcf
   - Purple: #985fb9
   - Dark: #09121f, #415169

3. **Statistics Display**:
   - Replacements Made counter
   - Active Mappings counter

4. **Toast Notifications**: User feedback for actions
   - Success messages (green)
   - Warning messages (purple)
   - Error messages (dark)

5. **Responsive Design**: Adapts to different screen sizes with mobile-friendly layout

## Technical Implementation

### File Structure
- Single HTML file: `prompt-sanitizer.html`
- Self-contained with inline CSS and JavaScript
- No external dependencies

### Key Technologies
- Pure HTML5, CSS3, JavaScript (ES6+)
- LocalStorage API for data persistence
- CSS Grid and Flexbox for layout
- CSS animations for smooth transitions

### Code Organization
- Modular JavaScript functions for:
  - Storage management
  - Rendering (mapping sets, editor)
  - Mapping operations (add, update, remove)
  - Sanitization/desanitization logic
  - UI state management

## Recent Enhancements (This Session)

### Completed Features
1. ✅ Case insensitivity support for all mappings
2. ✅ Collapsable mappings section with animated transitions
3. ✅ Auto-generated {ref N} replacement values for new mappings
4. ✅ Overlapping pattern handling (longest-first sorting)
5. ✅ Moved "Add Mapping" button to top of list
6. ✅ New mappings insert at top of array
7. ✅ Input box highlighting with replaced text visibility
8. ✅ Configurable highlight persistence (fade vs. persistent)
9. ✅ Resizable text containers (both vertical and horizontal)
10. ✅ Fixed output box styling to match input (font, spacing, newlines)

### Removed Features
- ❌ Side-by-side layout toggle (removed due to resize compatibility issues)

## Current State

### Working Features
- ✅ All core sanitize/desanitize functionality
- ✅ Mapping set management (create, delete, switch)
- ✅ CSV import
- ✅ Case-insensitive matching
- ✅ Overlapping pattern handling
- ✅ Wildcard email and phone detection
- ✅ Highlighting system with persistence option
- ✅ Resizable input/output containers
- ✅ LocalStorage persistence
- ✅ Collapsable UI sections
- ✅ Toast notifications
- ✅ Statistics tracking

### Known Limitations
- Resize functionality limited to vertical stacking layout only
- Phone number detection limited to US formats
- No undo/redo functionality
- No export functionality for mapping sets
- No dark mode

## Future Enhancement Opportunities
1. Export mapping sets to CSV/JSON
2. Regex pattern support in mappings
3. Multiple wildcard patterns (SSNs, credit cards, etc.)
4. Bulk operations on mappings
5. Mapping search/filter functionality
6. Keyboard shortcuts
7. Drag-and-drop mapping reordering
8. Mapping history/versioning
9. Dark mode theme
10. Multi-language support

## File Locations
- Application: `/Users/alhanger/Documents/Experient/Misc/prompt-sanitizer/prompt-sanitizer.html`
- Progress Log: `/Users/alhanger/Documents/Experient/Misc/prompt-sanitizer/PROGRESS_LOG.log`

## Git Status
- Current branch: main
- Status: Clean (all changes committed)
- Recent commits:
  - update README
  - add csv upload support
  - add highlighting feature on sanitize/desantize
  - update UI with Experient color palette
  - add wildcards feature

---
End of Progress Log
