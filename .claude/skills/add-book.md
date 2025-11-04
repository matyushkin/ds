# Add Book Skill

## Description
This skill helps add a new book to the appropriate section of the repository.

## Instructions for Claude

When a user wants to add a book, follow these steps:

1. **Determine the book category:**
   - Data Science (general) → `books/books_data_science.md`
   - Machine Learning → `books/books_machine_learning.md`
   - Neural Networks → `books/books_neural_networks.md`
   - Computer Vision → `books/books_computer_vision.md`
   - Geospatial Data → `books/books_geospatial.md`
   - Natural Language Processing → `books/books_nlp.md`
   - Financial Data Analysis → `books/books_finance.md`
   - Big Data → `books/books_big_data.md`

2. **Collect book information:**
   - Title (in English and Russian if available)
   - Author(s)
   - Publication year
   - Link to the book (if freely available)
   - Brief description (in Russian - repository language)
   - Difficulty level (beginner/intermediate/advanced)

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `books/` directory

4. **Identify the format:**
   Study the existing entry format in the file and use a similar format

5. **Add the book:**
   - Use the Edit tool to add the book to the appropriate section
   - Maintain consistent formatting
   - Add the book to a logical section (by level or topic)

6. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the book 'Python for Data Analysis' by Wes McKinney to the Data Science section"

You should:
1. Read `books/books_data_science.md`
2. Add the book in the correct format
3. Save the changes
4. Inform the user about the result

## Important Notes
- Descriptions should be in Russian (repository content language)
- Maintain the existing structure and formatting
- Ensure the book is added to the correct category
