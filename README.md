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

Think of a mapping set as a template for replacing text.

1. In the left sidebar, type a name like "My Contacts" in the text box
2. Click **"+ Add"**
3. Click **"+ Add Mapping"** at the bottom
4. Fill in what you want to replace:
   - **Original text:** `john@email.com`
   - **Replacement:** `[EMAIL_1]`
5. Add more mappings by clicking **"+ Add Mapping"** again

Everything saves automatically as you type.

### Step 2: Hide Sensitive Info (Sanitize)

1. Paste or type your text in the **"Input Text"** box on the right
2. Click **"🔒 Sanitize"**
3. Your text appears in the **"Output"** box with replacements made

**Example:**
- You type: "Contact john@email.com about the project"
- You get: "Contact [EMAIL_1] about the project"

### Step 3: Restore Original Text (Desanitize)

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

**Q: Do I need internet to use this?**
No, it works completely offline after you download it.

**Q: The file won't open properly**
Try right-clicking the HTML file and selecting "Open with" → Choose your web browser (Chrome, Firefox, Edge, or Safari).

**Q: Can I share this with my team?**
Yes! Just share the GitHub link. Each person will have their own local mappings.