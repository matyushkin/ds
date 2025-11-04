# Add Book Skill

## Description
This skill helps add a new book to the appropriate section of the repository. The repository is multilingual - books in any language are welcome with proper language flags.

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
   - Title (in original language)
   - Author(s)
   - Publication year
   - Link to the book (if freely available)
   - Language of the book (🇬🇧 English, 🇷🇺 Russian, 🇩🇪 German, 🇫🇷 French, 🇪🇸 Spanish, 🇨🇳 Chinese, 🇯🇵 Japanese, etc.)
   - Brief description (in the same language as the book)
   - Difficulty level (beginner/intermediate/advanced)

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `books/` directory

4. **Check for duplicates:**
   - Search the file content for the book title or author
   - If a similar entry is found, inform the user
   - Ask if they want to: update the existing entry, skip, or add anyway
   - If no duplicate found, proceed to the next step

5. **Identify the format:**
   Study the existing entry format in the file and use a similar format

6. **Add the book:**
   - Use the Edit tool to add the book to the appropriate section
   - Maintain consistent formatting
   - Add the book to a logical section (by level or topic)

7. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the book 'Python for Data Analysis' by Wes McKinney to the Data Science section"

You should:
1. Read `books/books_data_science.md`
2. Add the book in the correct format
3. Save the changes
4. Inform the user about the result

## Important Notes
- **Always start entries with a language flag emoji** (🇬🇧 🇷🇺 🇩🇪 🇫🇷 🇪🇸 🇨🇳 🇯🇵 etc.)
- Descriptions should be in the same language as the resource
- Maintain the existing structure and formatting
- Ensure the book is added to the correct category
- If the same book exists in multiple languages, list each version with its flag

## Format Examples

All entries must start with a language flag emoji. Common formats:

**Russian book:**
```markdown
🇷🇺 Флах П. Машинное обучение. Издательство, 2015 (описание на русском)
```

**English book:**
```markdown
🇬🇧 Hastie T., Tibshirani R. The Elements of Statistical Learning. Springer, 2009 (description in English)
```

**Book with translations:**
```markdown
🇬🇧 Goodfellow I. Deep Learning. MIT Press, 2016
🇷🇺 Перевод: Гудфеллоу Я. Глубокое обучение. ДМК Пресс, 2018
```

**With link:**
```markdown
🇬🇧 [Python for Data Analysis](https://example.com) by Wes McKinney (2017)
```

**Other languages (German, French, Chinese, etc.):**
```markdown
🇩🇪 Autor. Buchtitel. Verlag, 2020 (Beschreibung auf Deutsch)
🇫🇷 Auteur. Titre du livre. Éditeur, 2020 (description en français)
🇨🇳 作者. 书名. 出版社, 2020 (中文描述)
```

**Always match the existing format in the target file.**
