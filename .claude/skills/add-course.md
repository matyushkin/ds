# Add Course Skill

## Description
This skill helps add a new online course to the appropriate section of the repository.

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
   - Course title (in English and/or Russian)
   - Platform (Coursera, Stepik, YouTube, edX, etc.)
   - Instructor/Author
   - Course language (Russian/English)
   - Link to the course
   - Brief description (in Russian - repository language)
   - Difficulty level
   - Rating (if available)
   - Is the course free

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `courses/` directory

4. **Identify the format:**
   Study the existing entry format in the file and use a similar format

5. **Add the course:**
   - Use the Edit tool to add the course to the appropriate section
   - Group by platform or difficulty level if the file is organized that way
   - Maintain consistent formatting

6. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the course 'Machine Learning' by Andrew Ng on Coursera to the Machine Learning section"

You should:
1. Read `courses/courses_machine_learning.md`
2. Add the course in the correct format
3. Save the changes
4. Inform the user about the result

## Important Notes
- Descriptions should be in Russian (repository content language)
- Maintain the existing structure and formatting
- Ensure the course is added to the correct category
- Indicate if the course is free or paid
