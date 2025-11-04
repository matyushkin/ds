# Add Article Skill

## Description
This skill helps add a new article, blog post, or online publication to the appropriate section of the repository.

## Instructions for Claude

When a user wants to add an article, follow these steps:

1. **Determine the article category:**
   - Data Science (general) → `social/social_data_science.md`
   - Machine Learning → `social/social_machine_learning.md`
   - Neural Networks → `social/social_neural_networks.md`
   - Computer Vision → `social/social_computer_vision.md`
   - Geospatial Data → `social/social_geospatial.md`
   - Natural Language Processing → `social/social_nlp.md`
   - Big Data → `social/social_big_data.md`

2. **Collect article information:**
   - Article title (in original language)
   - Author(s)
   - Publication source (Medium, Habr, personal blog, etc.)
   - Publication date (if relevant)
   - Link to the article
   - Brief description (in Russian - repository language)
   - Article language (Russian/English)
   - Main topics covered
   - Difficulty level (beginner/intermediate/advanced)

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `social/` directory

4. **Identify the format:**
   Study the existing entry format in the file and use a similar format

5. **Add the article:**
   - Use the Edit tool to add the article to the appropriate section
   - Group by topic, source, or date if the file is organized that way
   - Maintain consistent formatting

6. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add an article about neural network optimization from Habr to the Neural Networks section"

You should:
1. Read `social/social_neural_networks.md`
2. Add the article in the correct format with title, author, link, and description
3. Save the changes
4. Inform the user about the result

## Important Notes
- Descriptions should be in Russian (repository content language)
- Maintain the existing structure and formatting
- Include the article language indicator if different from description
- Ensure the article link is accessible
- Add publication date if it's relevant for time-sensitive content
