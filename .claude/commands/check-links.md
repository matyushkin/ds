---
description: Validate all links in markdown files to check for broken or inaccessible URLs
---

# Check Links Command

You are helping validate links in the Data Science resources repository to identify broken or inaccessible URLs.

## Steps to Follow

1. **Determine scope:**
   Ask the user what they want to check:
   - All files in the repository
   - Specific directory (books, courses, data, social, software)
   - Specific topic (Data Science, ML, CV, NLP, etc.)
   - Specific file

2. **Find target files:**
   - Use Glob tool to locate markdown files based on scope
   - Example: `books/*.md` for all books, or `**/*.md` for all files

3. **Extract links:**
   - Read each file using Read tool
   - Extract all URLs matching patterns:
     - `http://...` and `https://...`
     - Markdown links: `[text](url)`
   - Create a deduplicated list of URLs to check
   - Keep track of which file(s) contain each URL

4. **Validate links:**
   For each unique URL:
   - Use `curl -I -L --max-time 10 <url>` to check HTTP status
   - Or use `wget --spider --timeout=10 <url>`
   - Categorize results:
     - ✓ Working (HTTP 200)
     - ⚠ Redirected (HTTP 301/302)
     - ✗ Broken (HTTP 4xx/5xx)
     - ⏱ Timeout
     - 🚫 Blocked/Other error

   Important: Add small delays between requests to avoid rate limiting

5. **Generate validation report:**
   Create a structured report with:

   ```
   Link Validation Report
   ======================
   Generated: [timestamp]
   Scope: [what was checked]

   Summary:
   - Total unique URLs: X
   - Working: X (XX%)
   - Redirected: X (XX%)
   - Broken: X (XX%)
   - Timeout/Error: X (XX%)

   Broken Links:
   [For each broken link:]
   - URL: <url>
     Status: <error>
     Found in: <file>:<line> (if available)

   Redirected Links:
   [For each redirected link:]
   - Original: <url>
     Redirects to: <final_url>
     Found in: <file>

   Timeout/Blocked:
   [List of URLs that couldn't be checked]
   ```

6. **Suggest actions:**
   - For broken links: suggest removal or finding alternatives
   - For redirects: suggest updating to final URL
   - For timeouts: suggest manual review

7. **Ask user about fixes:**
   - Do they want to update redirected links?
   - Do they want to remove broken links?
   - Do they want to save the report to a file?

## Important Notes
- Respect rate limits - add delays between checks (e.g., 1-2 seconds)
- Some sites may block automated requests - document these
- Don't modify files without explicit user confirmation
- Save the validation report for future reference
- Consider checking in batches to avoid overwhelming servers
- HEAD requests are more efficient than GET requests

## Implementation Tips
- Use a bash loop with curl for link checking
- Cache results to avoid rechecking the same URL
- Consider creating a `.link-check-cache.json` file
- Provide progress updates for large validation runs
