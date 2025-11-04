# Add Article Skill

## Description
This skill helps add a new article, blog post, or online publication to the appropriate section of the repository. Articles in any language are welcome with proper language flags.

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
   - Brief description (in the same language as the article)
   - Article language (🇬🇧 English, 🇷🇺 Russian, 🇩🇪 German, 🇫🇷 French, etc.)
   - Main topics covered
   - Difficulty level (beginner/intermediate/advanced)

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `social/` directory

4. **Check for duplicates:**
   - Search the file content for the article title or URL
   - If a similar entry is found, inform the user
   - Ask if they want to: update the existing entry, skip, or add anyway
   - If no duplicate found, proceed to the next step

5. **Identify the format:**
   Study the existing entry format in the file and use a similar format

6. **Add the article:**
   - Use the Edit tool to add the article to the appropriate section
   - Group by topic, source, or date if the file is organized that way
   - Maintain consistent formatting

7. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add an article about neural network optimization from Habr to the Neural Networks section"

You should:
1. Read `social/social_neural_networks.md`
2. Add the article in the correct format with title, author, link, and description
3. Save the changes
4. Inform the user about the result

## Important Notes
- **Always start entries with a language flag emoji** (🇬🇧 🇷🇺 🇩🇪 🇫🇷 etc.)
- Descriptions should be in the same language as the article
- Maintain the existing structure and formatting
- Ensure the article link is accessible
- Add publication date if it's relevant for time-sensitive content

## Format Examples

All entries must start with a language flag emoji:

**Russian article:**
```markdown
🇷🇺 [Введение в нейронные сети](https://habr.com/...) – обзор основных архитектур и их применение
```

**English article:**
```markdown
🇬🇧 [Understanding Transformers](https://medium.com/...) by Author Name – deep dive into attention mechanisms
```

**With date:**
```markdown
🇷🇺 [Новые подходы в NLP](https://url) (Иванов И., 2024) – обзор последних достижений
```

**Other languages:**
```markdown
🇩🇪 [Machine Learning Grundlagen](https://url) – Einführung in ML-Konzepte
```

**Always match the existing format in the target file.**
