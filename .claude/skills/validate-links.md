# Validate Links Skill

## Description
This skill helps validate all links in the markdown files to ensure they are accessible and not broken.

## Instructions for Claude

When a user wants to validate links, follow these steps:

1. **Determine scope:**
   Ask the user if they want to check:
   - All files in the repository
   - Specific category (books, courses, data, social, software)
   - Specific topic (Data Science, ML, CV, NLP, etc.)
   - Specific file

2. **Find all relevant markdown files:**
   - Use Glob tool to find markdown files: `**/*.md`
   - Filter based on the chosen scope

3. **Extract links from markdown files:**
   - Read each file using the Read tool
   - Extract all URLs (http:// and https://)
   - Parse markdown link syntax: `[text](url)`
   - Create a list of unique URLs to check

4. **Validate links:**
   For each URL:
   - Use WebFetch tool to check if the URL is accessible
   - Note: Some URLs may block automated requests, so handle failures gracefully
   - Track: accessible, broken (4xx/5xx errors), redirected, timeout
   - Consider rate limiting to avoid being blocked

5. **Generate report:**
   Create a summary with:
   - Total links checked
   - Number of working links
   - List of broken links with file locations
   - List of redirected links
   - List of timeouts or inaccessible links

6. **Suggest fixes:**
   For broken links:
   - Try to find alternatives (Internet Archive, updated URLs)
   - Suggest removing if permanently dead
   - Flag for manual review if uncertain

7. **Inform the user:**
   Provide the validation report and suggested actions

## Usage Example

User: "Check all links in the courses directory"

You should:
1. Find all files: `courses/*.md`
2. Extract all URLs from these files
3. Validate each URL
4. Generate a report showing working and broken links
5. Suggest fixes for broken links

## Important Notes
- Be respectful of rate limits - add delays between checks if needed
- Some sites may block automated requests - document these separately
- Don't modify files without user confirmation
- Provide clear file paths and line numbers for broken links
- Consider using HEAD requests instead of GET to be more efficient
- Handle authentication-required links appropriately
- Document the validation timestamp

## Implementation Tips
- Use bash `curl` or `wget` for link checking if WebFetch has limitations
- Consider checking in batches to avoid overwhelming servers
- Cache results to avoid rechecking the same URL multiple times
- Create a validation log file for future reference
