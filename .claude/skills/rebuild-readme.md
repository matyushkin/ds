# Rebuild README Skill

## Description
This skill helps rebuild the main README.md file from individual markdown files, creating a comprehensive table of contents.

## Instructions for Claude

When a user wants to rebuild the README, follow these steps:

1. **Understand the structure:**
   The repository uses a matrix structure:
   - **Rows (Topics)**: Data Science, Machine Learning, Neural Networks, Computer Vision, Geospatial, NLP, Finance, Big Data
   - **Columns (Resource Types)**: Courses, Books, Data, Social, Software
   - Each cell contains a link to a corresponding markdown file (e.g., `courses/courses_machine_learning.md`)

2. **Check for the Jupyter notebook tool:**
   Look for `main_readme_constructor.ipynb` in the root directory:
   - If it exists, this notebook may be used to auto-generate the README
   - Read the notebook to understand its logic
   - Consider running it if appropriate: `jupyter nbconvert --to notebook --execute main_readme_constructor.ipynb`

3. **Read existing README.md:**
   Use the Read tool to understand the current structure and format

4. **Gather all resource files:**
   - Use Glob tool to find all markdown files in: `books/`, `courses/`, `data/`, `social/`, `software/`
   - Organize them by category

5. **Build the table structure:**
   Create a markdown table with:
   - Header row: | Topic | Courses | Books | Data | Social | Software |
   - One row per topic area
   - Each cell contains a link to the corresponding markdown file
   - Use emojis or icons if present in the original README

6. **Add additional sections:**
   - Introduction/description
   - How to contribute
   - License information
   - Contact information (Telegram, GitHub)
   - Any other sections from the original README

7. **Write the new README:**
   - Use the Write tool to update `README.md`
   - Ensure proper markdown formatting
   - Maintain the existing style and tone

8. **Inform the user:**
   Show what was updated and provide a summary of changes

## Usage Example

User: "Rebuild the README to reflect all current resources"

You should:
1. Read `main_readme_constructor.ipynb` if it exists
2. Scan all resource directories
3. Create updated table with all categories and links
4. Update README.md
5. Inform the user about the result

## Important Notes
- Preserve the existing style and formatting
- Maintain Russian language for descriptions
- Ensure all links are correctly formatted
- Keep the matrix/table structure
- Include all metadata (license, contribution guidelines, etc.)
- If using the Jupyter notebook, verify its output before applying
