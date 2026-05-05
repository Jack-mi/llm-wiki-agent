Save an article from a URL to the raw/ directory, with automatic format conversion.

Usage: /wiki-save $URL

$URL can be:
- WeChat official account article (mp.weixin.qq.com)
- Any other web article URL
- Local file path (will be copied to raw/)

The command will:
1. Detect the source type (WeChat vs other web vs local file)
2. Download/fetch the content
3. Convert to clean Markdown format
4. Extract the article title
5. Generate a kebab-case filename
6. Save to raw/articles/ directory
7. Report the saved file path

## Implementation Strategy

### For WeChat articles (mp.weixin.qq.com):
Use the specialized workflow from memory (reference_wechat_article_fetch.md):
1. curl with User-Agent to download HTML
2. markitdown to convert to Markdown
3. Extract title and create kebab-case filename
4. Save to raw/articles/

### For other web URLs:
1. Try WebFetch first with prompt: "Extract the full article content including title, author, publication date, and main text. Convert to clean markdown format."
2. If WebFetch fails (network restrictions), fall back to curl + markitdown
3. Extract title and create kebab-case filename
4. Save to raw/articles/

### For local files:
1. Check if file exists
2. If non-markdown, use markitdown to convert
3. Copy/convert to raw/ with appropriate subdirectory based on file type
4. Preserve original filename or generate from content

## Output

After successful save, print:
- Saved file path
- Article title
- File size and line count
- Suggest next step: `/wiki-ingest <saved-path>`

## Error Handling

- If download fails, report the error and suggest manual download
- If title extraction fails, prompt user for filename
- If file already exists, ask user whether to overwrite
