# Add Dataset Skill

## Description
This skill helps add a new dataset or data source to the appropriate section of the repository. Datasets can be documented in any language with proper language flags.

## Instructions for Claude

When a user wants to add a dataset, follow these steps:

1. **Determine the dataset category:**
   - Data Science (general) → `data/data_data_science.md`
   - Machine Learning → `data/data_machine_learning.md`
   - Computer Vision → `data/data_computer_vision.md`
   - Geospatial Data → `data/data_geospatial.md`
   - Natural Language Processing → `data/data_nlp.md`
   - Financial Data Analysis → `data/data_finance.md`

   Note: There may not be separate data files for Neural Networks and Big Data

2. **Collect dataset information:**
   - Dataset name
   - Source/Platform (Kaggle, UCI ML Repository, Google Dataset Search, etc.)
   - Link to the dataset
   - Dataset language/documentation (🇬🇧 English, 🇷🇺 Russian, etc.)
   - Brief description (in the same language): what it contains, what tasks it's suitable for
   - Dataset size (if known)
   - Data format (CSV, JSON, Images, etc.)
   - License (if important)
   - Application area

3. **Read the existing file:**
   Use the Read tool to read the corresponding file in the `data/` directory

4. **Check for duplicates:**
   - Search the file content for the dataset name or similar datasets
   - If a similar entry is found, inform the user
   - Ask if they want to: update the existing entry, skip, or add anyway
   - If no duplicate found, proceed to the next step

5. **Identify the format:**
   Study the existing entry format in the file and use a similar format

6. **Add the dataset:**
   - Use the Edit tool to add the dataset to the appropriate section
   - Group by data type or application area
   - Maintain consistent formatting

7. **Inform the user:**
   Show what was added and to which file

## Usage Example

User: "Add the MNIST dataset to the Computer Vision section"

You should:
1. Read `data/data_computer_vision.md`
2. Add the dataset with description and link
3. Save the changes
4. Inform the user about the result

## Important Notes
- **Always start entries with a language flag emoji** (🇬🇧 🇷🇺 etc.) based on dataset documentation language
- Descriptions should be in the same language as the dataset documentation
- Maintain the existing structure and formatting
- Include relevant metadata (size, format, license)
- Ensure the dataset link is accessible

## Format Examples

All entries must start with a language flag emoji:

**English dataset:**
```markdown
🇬🇧 [MNIST Dataset](http://yann.lecun.com/exdb/mnist/) – handwritten digits for image classification tasks (60k training, 10k test images)
```

**Russian dataset:**
```markdown
🇷🇺 [Датасет отзывов на товары](https://kaggle.com/...) – корпус отзывов для анализа тональности (формат: CSV, 100k записей)
```

**With metadata:**
```markdown
🇬🇧 [ImageNet](http://www.image-net.org/) (format: images, size: 150GB) – large-scale image database for object recognition
```

**Always match the existing format in the target file.**
