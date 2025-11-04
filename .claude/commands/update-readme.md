---
description: Update the main README.md file to reflect current repository structure
---

# Update README Command

You are helping update the main README.md file to reflect the current state of the Data Science resources repository.

## Steps to Follow

1. **Check for automated tool:**
   - Look for `main_readme_constructor.ipynb` in the root directory
   - If it exists, ask the user if they want to use it or do a manual update

2. **If using the Jupyter notebook:**
   - Read the notebook to understand its logic
   - Execute it: `jupyter nbconvert --to notebook --execute main_readme_constructor.ipynb`
   - Verify the output
   - Ask user to confirm before applying changes

3. **If doing manual update:**

   a. **Read current README.md** to understand the structure

   b. **Scan all resource directories:**
      - Use Glob to find all files in: `books/`, `courses/`, `data/`, `social/`, `software/`
      - Organize by category

   c. **Build the resource table:**
      - Create markdown table with Topics as rows and Resource Types as columns
      - Each cell should link to the corresponding markdown file
      - Topics: Data Science, ML, Neural Networks, CV, Geospatial, NLP, Finance, Big Data
      - Resource Types: Courses, Books, Data, Social, Software

   d. **Preserve existing sections:**
      - Introduction/Welcome message
      - How to contribute guidelines
      - Community links (Telegram, etc.)
      - License information
      - Author/Maintainer information

   e. **Update the README:**
      - Use Write tool to update README.md
      - Maintain Russian language for text
      - Keep existing style and emojis if present

4. **Verify the result:**
   - Read the updated README.md
   - Check that all links are correctly formatted
   - Ensure table renders properly

5. **Inform the user:**
   - Show a summary of what was updated
   - Highlight any new resources added to the table

## Important Notes
- Preserve the existing writing style and tone
- Maintain Russian language throughout
- Ensure all internal links work correctly
- Keep the table structure clear and readable
- Don't remove any existing sections without user confirmation
