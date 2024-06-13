# Symbiota Docs Documentation Style Guide
Please refer to and update this style guide to help maintain consistency across the user documentation for [Symbiota](https://github.com/BioKIC/Symbiota).

## Page-level Frontmatter
Each page in Symbiota Docs should contain the following elements, some of which format the citation that appears at the bottom of each page:
```
title: "Page Title in Title Case"
date: 20XX-MM-DD
weight: #
draft: false
authors: ["Firstname Lastname"]
keywords: ["x", "y", "z", "etc"]
```
- `date` should refer to the first day that the page was created, not modified (see below).
- Title values shoule be succicent and often reflect an action, e.g. "Deleting Records".

If a page is modified, add values for `lastmod` and `editors`:
```
lastmod: 20XX-MM-DD
editors: ["Firstname Lastname"]
```

Include a weight value (an integer) to organize the order in which a page's title appears within the left-hand navigation menu in Symbiota Docs:
```
weight: #
```

## Formatting Conventions

Introduce the topic on a page using classes, e.g.
```
{{< notice info >}}
  This Symbiota Docs page is about...
{{</ notice >}}
```
Or to add tips:
```
{{< notice tip >}}
  Here's a tip about this feature...
{{</ notice >}}
```

Use _italics_ for
- Filenames, e.g. _identifications.csv_  
- Names of columns/fields, e.g. _Additional Identifier Value_ or _basisOfRecord_
- File and navigation paths, paired with carrots, e.g. _My Profile > Occurrence Management > Administration Control Panel_ or _Sitemap > Additional Resources > Glossary_

Use quotation marks `"..."` when referencing:
- Example values, e.g. "PreservedSpecimen"
- Buttons, e.g. "Create/Refresh Darwin Core Archive"

Use capitalization for:
- Tabs, e.g. Traits tab
- Modules, e.g. Material Sample module

Use **bold** for:
- emphasis, e.g. "Before batch editing, remember to **backup your dataset**".

Additionally:
- Top-level headings within documentation pages should use `##` and should generally use title case.
- Format code snippets with \`...\`, e.g. `bundle exec jekyll serve`.
- File extensions written as part of a filename are lowercase, e.g. *example.jpg*, but when written alone are uppercase, e.g. "The file should be a JPG."

## Including Media
To include a basic image with a caption, do so e.g.:
```
{% include figure image_path="/symbiota-docs/static/images/edittaxon.png" alt="alt text goes here" caption="Figure caption text goes here." %}
```

```
| ![Image Title](/symbiota-docs/images/filename.png) |
|:--:|
| Caption. |
```

To include a basic image without a caption, do so e.g.:
```
![Image Title](/symbiota-docs/images/filename.png)
```
To resize, align, or add an alt attribute (for screenreaders) to an image:
```
<img src="/symbiota-docs/static/images/filename.png" alt="This image shows XYZ" width="100"/>{: .align-right}
```

To include a video, do so e.g.:
```
{{< youtube ed2VEZCJwEI >}}
```

## Naming Files
Markdown files (.md) being added to Symbiota Docs should be named descriptively yet succinctly. Do not use any character other than `a-z`.

Image files should be named descriptively in lowercase. Do not use any character other than `a-z`, `-`, or `_`. Images (.png, .jpg) should be saved to `/symbiota-docs/tree/master/static/images`.

## Related Resources
- [GitHub Formatting Syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Markdown Emojis Directory](https://gist.github.com/rxaviers/7360908)
