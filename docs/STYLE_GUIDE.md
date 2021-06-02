# Style guide

Writing style is about consistency and readability.
Inconsistent formatting, punctuation, and capitalization
can be distracting to readers.
Following a consistent style helps our content get the attention it deserves.

Note: Style is not voice.
Individual blog post authors should use their own voice.
See the sections on [**English language spelling**](#English-language-spelling)
and [**Date and time**](#Date-and-time)

In general, the site (more or less) follows the
[Microsoft style guide](https://docs.microsoft.com/en-us/style-guide/welcome/).
Check out the article
["Top 10 tips for Microsoft style and voice,"](https://docs.microsoft.com/en-us/style-guide/top-10-tips-style-voice)
which is a great starting point for new authors.

## Accessibility

Web accessibility is not a style choice, it's a requirement.
Still, this is a good place to include some reminders for authors.

If you're drafting some content and you're not sure how to make it accessible,
we're happy to help you!
Please make a note in your pull request that you need assistance.

### Include descriptive alt-text for any images

Check out this
[image alt-text guide from WebAIM](https://webaim.org/techniques/alttext/).

### Use meaningful link descriptions

Check out this
[link description guide from WebAIM](https://webaim.org/techniques/hypertext/).

Main points:

- Don't use phrases such as "click here," "more," or "click for details,"
  which are ambiguous when read out of context
- Place the distinguishing information of links at the beginning of a link
- Use link words and phrases that make sense if the link is read
  without the surrounding text

## Semantic line breaks

To facilitate review and editing with Git and various text editors,
please use [semantic line breaks](https://sembr.org).

How it works: if a single line is going to extend beyond column 80,
rather than breaking right at column 80,
you should add a line break at a natural point in the sentence.
For example: after a comma, before a conjunction (and/or/but),
or before a link with a long url.

Here's a raw example of what semantic line breaks for links look like:

```markdown
If you use VSCode, consider installing the
[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
extension.
You can find the full list of rules in
[the project's Rules.md](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md)
file.
```

Note that in this case, the long urls extend beyond column 80,
but the main content sits comfortably in the desired area.

## Markdown editing

When contributing content, most of what you need to know is described in the
[Markdown basic syntax guide](https://www.markdownguide.org/basic-syntax/).

If you use VSCode, consider installing the
[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
extension.
You can find the full list of rules in
[the project's Rules.md](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md)
file.
Don't worry about memorizing them all.
Most inconsistencies will be caught at the PR stage.

Some rules to know, to save you revision time:

- Don't embed HTML in a markdown doc, the linter doesn't approve
  (note: if you want more sophisticated layouts or styling on a page,
  open an issue to ask about adding a
  [Hugo shortcode](https://gohugo.io/templates/shortcode-templates/)
  or [partial template](https://gohugo.io/templates/partials/))
- The page title is always a header level 1 (H1, a single pound sign `#`),
  so the first header level in any content is an H2 (double pound sign `##`)
- For headers, put a space after the pound signs (`##`), before the text
- Add blank lines around headers, lists, blockquotes, and code blocks
- Don't skip header levels (e.g. H2 to H4)
- Prefer hyphens (`-`) to asterisks (`*`) for unordered lists
- Don't put punctuation at the end of a header
- Don't put punctuation at the end of list items
  (note: if your lists items contain multiple sentences,
  consider whether they should be a list in the first place)

## Formatting

To reduce visual noise, please avoid using many different kinds of formatting.
Keywords should be **bold** (`**bold**`).
These get rendered with `<strong>` semantic tags.

Avoid using _italics_ (`_italics_` or `*italics*`) for emphasis.
These get rendered with `<em>` (emphasis) semantic tags.
[Bold is more visually distinct than italic for sans-serif fonts](https://practicaltypography.com/bold-or-italic.html),
which makes it a better formatting choice for web content
where people tend to skim.

Non-English words should be _italicized_.
To italicize a word in Markdown,
surround the word with underscores (`_`),
one at the beginning and another at the end: `_italicized_`

Only use CAPS for words that are actually capitalized
like SQL operations ("SELECT") or abbreviations ("LGBTQ").

## English language spelling

Outside of blog posts, please use US English spelling.

### Blog posts

For words with regional spelling variations,
for example "color" vs. "colour,"
blog post authors should use the variant that is natural for them.

## Date and time

To ensure dates are friendly to an international audience,
please follow these guidelines.

In prose, spell out the date in full. For example:

- `January 1, 2021`
- `January 1st, 2021`
- `1 January 2021`

[The Microsoft style guide date guidelines](https://docs.microsoft.com/en-us/style-guide/a-z-word-list-term-collections/term-collections/date-time-terms)
are more strict about date formats.
For ADHDevOps blog content,
authors can use their preferred format of the ones listed above.

For numeric dates, use
[ISO 8601 style](https://en.wikipedia.org/wiki/ISO_8601),
ordered year-month-day, e.g. `2021-01-01`.

## Key terminology

For words we're likely to use frequently,
please follow the spelling, capitalization, and punctuation here:

- ADHDevOps (when referencing the greater community)
- ADHDevOps.club (when referencing this website)
- DevOps (unless capitalized differently as part of a proper noun)
- DevOops! (with or without the exclamation point)

(Please suggest other terms we should list here!)

If you're unsure how to capitalize a specific term
and it's not listed in the [Microsoft style guide](https://docs.microsoft.com/en-us/style-guide/),
try searching Wikipedia for an example where it's used in a sentence.
(So, not the page title or the first word of a sentence,
which usually get capitalized no matter what.)
