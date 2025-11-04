# Add Software Skill

## Description
This skill helps add a new library, framework, or tool to the appropriate section of the repository. Software can be documented in any language with proper language flags.

## Instructions for Claude

When a user wants to add software, follow these steps:

1. **Determine the software category:**
   - Data Science (general) → `software/software_data_science.md`
   - Machine Learning → `software/software_machine_learning.md`
   - Neural Networks → `software/software_neural_networks.md`
   - Computer Vision → `software/software_computer_vision.md`
   - Geospatial Data → `software/software_geospatial.md`
   - Natural Language Processing → `software/software_nlp.md`
   - Big Data → `software/software_big_data.md`

2. **Collect software information:**
   - Library/framework/tool name
   - Programming language (Python, R, Julia, etc.)
   - Link to GitHub or official website
   - Link to documentation
   - Documentation language (🇬🇧 English, 🇷🇺 Russian, etc.)
   - Brief description of purpose (in the same language as documentation)
   - Main features/capabilities
   - Popularity (GitHub stars, if relevant)
   - Dependencies or requirements
   - Usage examples (if available)

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `software/` directory

4. **Check for duplicates:**
   - Search the file content for the software/library name
   - If a similar entry is found, inform the user
   - Ask if they want to: update the existing entry, skip, or add anyway
   - If no duplicate found, proceed to the next step

5. **Identify the format:**
   Study the existing entry format in the file and use a similar format

6. **Add the software:**
   - Use the Edit tool to add to the appropriate section
   - Group by type (libraries, frameworks, tools)
   - Maintain consistent formatting
   - Ensure links are working

7. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the scikit-learn library to the Machine Learning section"

You should:
1. Read `software/software_machine_learning.md`
2. Add the library with description, links to GitHub and documentation
3. Save the changes
4. Inform the user about the result

## Important Notes
- **Always start entries with a language flag emoji** (🇬🇧 🇷🇺 etc.) based on documentation language
- Descriptions should be in the same language as the documentation
- Maintain the existing structure and formatting
- Include links to both repository and documentation
- Mention the programming language
- Add relevant metadata (popularity, license)

## Format Examples

All entries must start with a language flag emoji:

**English library:**
```markdown
🇬🇧 [scikit-learn](https://github.com/scikit-learn/scikit-learn) ([docs](https://scikit-learn.org)) – machine learning library for Python (⭐60k stars)
```

**Russian library:**
```markdown
🇷🇺 [pymorphy2](https://github.com/kmike/pymorphy2) – морфологический анализатор для русского языка (Python)
```

**With metadata:**
```markdown
🇬🇧 [TensorFlow](https://github.com/tensorflow/tensorflow) (Python/C++, ⭐185k) – end-to-end platform for machine learning
```

**Always match the existing format in the target file.**
