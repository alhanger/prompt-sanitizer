# Prompt Sanitizer/Desanitizer - User Guide

Hide sensitive information in your text and restore it later.

## 📥 Getting Started

### Download and Open

1. Click the green **"Code"** button at the top of this page
2. Click **"Download ZIP"**
3. Find the downloaded ZIP file in your Downloads folder
4. Right-click it and select **"Extract All"** (Windows) or just double-click it (Mac)
5. Open the extracted folder and double-click the HTML file

The app will open in your web browser. That's it!

## 🎯 How to Use

### Step 1: Create a Mapping Set

Think of a mapping set as a template for replacing text. You can create one manually or import from a CSV file.

#### Option A: Create Manually

1. In the left sidebar, type a name like "My Contacts" in the text box
2. Click **"+ Add"**
3. Click **"+ Add Mapping"** at the bottom
4. Fill in what you want to replace:
   - **Original text:** `john@email.com`
   - **Replacement:** `[EMAIL_1]`
5. Add more mappings by clicking **"+ Add Mapping"** again

#### Option B: Import from CSV

1. Prepare a CSV file with two columns:
   - Column 1: Original text (what you want to replace)
   - Column 2: Replacement text (what to replace it with)
2. Click **"📁 Upload CSV"** in the left sidebar
3. Select your CSV file
4. The app will automatically create a mapping set named after your file

**CSV Example:**
```
Original,Replacement
john@email.com,[EMAIL_1]
jane.doe@company.com,[EMAIL_2]
555-1234,[PHONE]
John Smith,[NAME_1]
```

Your CSV can include or skip the header row - the app will detect it automatically.

Everything saves automatically as you type.

### Step 2: Use Wildcard Options (Optional)

For quick sanitization without creating individual mappings:

- **All Emails** - Automatically replaces any email address with `[email]`
- **All Phone Numbers** - Automatically replaces phone numbers with `[phone]`

Check these boxes in the left sidebar to enable them. They work alongside your custom mappings.

### Step 3: Hide Sensitive Info (Sanitize)

1. Paste or type your text in the **"Input Text"** box on the right
2. Click **"🔒 Sanitize"**
3. Your text appears in the **"Output"** box with replacements made
4. Replaced words will be briefly highlighted in yellow so you can see what changed

**Example:**
- You type: "Contact john@email.com about the project"
- You get: "Contact [EMAIL_1] about the project"

### Step 4: Restore Original Text (Desanitize)

1. Paste the sanitized text into the **"Input Text"** box
2. Click **"🔓 Desanitize"**
3. Your original text is restored in the **"Output"** box

### Other Helpful Buttons

- **📋 Copy Output** - Copy the result to your clipboard
- **🗑️ Clear All** - Erase both text boxes (doesn't delete your mappings)

## 💾 Your Data

- Everything is saved in your browser - nothing goes to the internet
- Your mappings will be there next time you open the app
- Works completely offline
- Only you can see your data

**⚠️ Important:** If you clear your browser history/data, you'll lose your mappings.

## ❓ Common Questions

**Q: Can I have multiple mapping sets?**
Yes! Create different sets for different purposes and switch between them by clicking on their names.

**Q: How do I delete a mapping?**
Click the **×** button next to any mapping or mapping set you want to remove.

**Q: What CSV format should I use?**
Your CSV should have two columns. The first column is the original text, and the second is the replacement. You can include a header row (like "Original,Replacement") or skip it - the app auto-detects headers. The app handles quoted values and commas within text properly.

**Q: Can I upload the same CSV multiple times?**
Yes! Each upload creates a new mapping set, so you can import the same CSV with different modifications or keep multiple versions.

**Q: Do wildcard options work with desanitize?**
No, wildcards only work for sanitizing. To restore wildcard replacements like `[email]` and `[phone]`, you need to create explicit mappings in your set.

**Q: Do I need internet to use this?**
No, it works completely offline after you download it.

**Q: The file won't open properly**
Try right-clicking the HTML file and selecting "Open with" → Choose your web browser (Chrome, Firefox, Edge, or Safari).

**Q: Can I share this with my team?**
Yes! Just share the GitHub link. Each person will have their own local mappings. You can also share CSV files with teammates so they can import the same mapping sets.