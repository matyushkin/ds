# Add Course Skill

## Description
This skill helps add a new online course to the appropriate section of the repository. The repository is multilingual - courses in any language are welcome with proper language flags.

## Instructions for Claude

When a user wants to add a course, follow these steps:

1. **Determine the course category:**
   - Data Science (general) → `courses/courses_data_science.md`
   - Machine Learning → `courses/courses_machine_learning.md`
   - Neural Networks → `courses/courses_neural_networks.md`
   - Computer Vision → `courses/courses_computer_vision.md`
   - Geospatial Data → `courses/courses_geospatial.md`
   - Natural Language Processing → `courses/courses_nlp.md`
   - Financial Data Analysis → `courses/courses_finance.md`
   - Big Data → `courses/courses_big_data.md`

2. **Collect course information:**
   - Course title (in original language)
   - Platform (Coursera, Stepik, YouTube, edX, etc.)
   - Instructor/Author
   - Course language (🇬🇧 English, 🇷🇺 Russian, 🇩🇪 German, 🇫🇷 French, 🇪🇸 Spanish, 🇨🇳 Chinese, etc.)
   - Link to the course
   - Brief description (in the same language as the course)
   - Difficulty level
   - Rating (if available)
   - Is the course free

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `courses/` directory

4. **Check for duplicates:**
   - Search the file content for the course title or instructor
   - If a similar entry is found, inform the user
   - Ask if they want to: update the existing entry, skip, or add anyway
   - If no duplicate found, proceed to the next step

5. **Identify the format:**
   Study the existing entry format in the file and use a similar format

6. **Add the course:**
   - Use the Edit tool to add the course to the appropriate section
   - Group by platform or difficulty level if the file is organized that way
   - Maintain consistent formatting

7. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the course 'Machine Learning' by Andrew Ng on Coursera to the Machine Learning section"

You should:
1. Read `courses/courses_machine_learning.md`
2. Add the course in the correct format
3. Save the changes
4. Inform the user about the result

## Important Notes
- **Always start entries with a language flag emoji** (🇬🇧 🇷🇺 🇩🇪 🇫🇷 🇪🇸 🇨🇳 etc.)
- Descriptions should be in the same language as the resource
- Maintain the existing structure and formatting
- Ensure the course is added to the correct category
- Indicate if the course is free or paid

## Format Examples

All entries must start with a language flag emoji. Common formats:

**Russian course:**
```markdown
🇷🇺 [Введение в машинное обучение](https://stepik.org/course/123) (Stepik, ★4.9)
```

**English course:**
```markdown
🇬🇧 [Machine Learning Specialization](https://coursera.org/...) by Andrew Ng (Coursera, free with certificate option)
```

**With description:**
```markdown
🇷🇺 [Курс по Deep Learning](https://url) (YouTube, ВШЭ) – основы нейронных сетей и их применение
```

**Other languages:**
```markdown
🇩🇪 [Maschinelles Lernen](https://url) (Plattform, Universität) – Einführung in ML
🇫🇷 [Apprentissage Automatique](https://url) (Plateforme) – cours d'introduction
```

**Always match the existing format in the target file.**
