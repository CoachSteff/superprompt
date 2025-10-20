# Example 4: Documentation Cleanup (Markdown Librarian)

**Why this works:** Highly constrained task with clear success criteria and refusal rules. The structured output is immediately committable to a repo.

**Quick customization levers:**
1. Change documentation type (API docs, user guides, technical specs)
2. Adjust cleanup scope (fix formatting, rewrite unclear sections, reorganize structure)
3. Modify style guide (formal, conversational, minimalist)

---

```markdown
Title: Documentation Librarian Pass

ROLE & TONE
You are a technical documentation editor. Write with precision and clarity. Prioritize readability and consistency over clever phrasing.

INTENT
Clean up the provided markdown documentation file to make it readable, consistent, and navigable. Success means: (1) all headers follow a consistent hierarchy, (2) code blocks are properly formatted, (3) links are valid, (4) the structure is logical, (5) the tone is consistent throughout.

CONTEXT
- File type: Markdown (.md) documentation for a software project
- Target audience: Developers who are new to the project
- Current problems: Inconsistent header levels, broken links, code blocks without language tags, mix of formal and casual tone
- Style guide:
  - Use sentence case for headers (not title case)
  - Code blocks must include language tags (```python, ```javascript, etc.)
  - Links should be descriptive, not "click here"
  - Tone: Professional but approachable (avoid jargon, use "you" instead of "the user")
- Constraints: Do not change the meaning of technical content; only fix formatting and structure

REASONING POLICY
1. First pass: Fix all markdown formatting issues (headers, code blocks, lists, links)
2. Second pass: Check header hierarchy (H1 → H2 → H3, no skips)
3. Third pass: Verify all links and flag any broken ones
4. Fourth pass: Standardize tone (rewrite overly formal or overly casual sections)
5. Refuse to rewrite technical content unless it's factually incorrect or unclear
6. Refuse to add new sections or content not present in the original
7. If a link is broken and you can't infer the correct target, flag it with [BROKEN LINK: description]

OUTPUT
Produce two things:

1. **Cleaned markdown file** (the full edited document, ready to commit)
2. **Change log** (a bulleted list of all changes made, organized by category: Formatting, Structure, Tone, Links)

SELF-CHECK
Before finalizing:
- Are all code blocks tagged with a language?
- Do headers follow a logical hierarchy with no skips?
- Is the tone consistent throughout?
- Are all links descriptive and functional (or flagged if broken)?
```

---

**Example Input:**

```markdown
# Getting Started

Welcome to the project!!

## install

Run this:

```
npm install my-package
```

## How To Use It

You can use it like this:

```
const pkg = require('my-package');
pkg.run();
```

For more info [click here](http://broken-link.com).

### Configuration

You have several options for configuration. The user can set these in a config file.

1. `option1` - does something
2. `option2` - does something else

# Advanced Usage

This section covers advanced topics.

## Custom Scripts

You can write custom scripts like so:

```
function myScript() {
  console.log('Hello');
}
```
```

---

**Example Output:**

## 1. Cleaned Markdown File

```markdown
# Getting started

Welcome to the project.

## Installation

Run this command to install the package:

```bash
npm install my-package
```

## Usage

You can use the package in your project like this:

```javascript
const pkg = require('my-package');
pkg.run();
```

For more information, see the [BROKEN LINK: detailed usage guide].

## Configuration

You have several options for configuration. You can set these in a config file:

1. `option1` – Does something
2. `option2` – Does something else

## Advanced usage

This section covers advanced topics.

### Custom scripts

You can write custom scripts like this:

```javascript
function myScript() {
  console.log('Hello');
}
```
```

---

## 2. Change Log

**Formatting:**
- Fixed header hierarchy: Changed "# Advanced Usage" to "##" (should be H2, not H1)
- Added language tags to all code blocks (bash, javascript)
- Standardized list formatting (added em dash after backticked terms)

**Structure:**
- Changed "How To Use It" to "Usage" for consistency with typical documentation conventions
- Changed "install" to "Installation" (proper sentence case)
- Moved "Custom Scripts" under "Advanced usage" as H3 (was incorrectly at H2)

**Tone:**
- Removed double exclamation marks ("project!!" → "project.")
- Changed "The user can set these" to "You can set these" (direct address, per style guide)
- Removed unnecessary capitalization in "Advanced Usage" → "Advanced usage"

**Links:**
- Flagged broken link: [BROKEN LINK: detailed usage guide] (original URL was http://broken-link.com)
- Changed link text from "click here" to descriptive text

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
