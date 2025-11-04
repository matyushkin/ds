# Add Software Skill

## Description
This skill helps add a new library, framework, or tool to the appropriate section of the repository.

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
   - Brief description of purpose (in Russian - repository language)
   - Main features/capabilities
   - Popularity (GitHub stars, if relevant)
   - Dependencies or requirements
   - Usage examples (if available)

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `software/` directory

4. **Identify the format:**
   Study the existing entry format in the file and use a similar format

5. **Add the software:**
   - Use the Edit tool to add to the appropriate section
   - Group by type (libraries, frameworks, tools)
   - Maintain consistent formatting
   - Ensure links are working

6. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the scikit-learn library to the Machine Learning section"

You should:
1. Read `software/software_machine_learning.md`
2. Add the library with description, links to GitHub and documentation
3. Save the changes
4. Inform the user about the result

## Important Notes
- Descriptions should be in Russian (repository content language)
- Maintain the existing structure and formatting
- Include links to both repository and documentation
- Mention the programming language
- Add relevant metadata (popularity, license)
