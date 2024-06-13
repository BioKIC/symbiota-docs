# Symbiota Docs Documentation Style Guide

Please refer to and update this style guide to help maintain consistency across the user documentation for [Symbiota](https://github.com/BioKIC/Symbiota). 

## Formatting conventions

Top-level headings within documentation pages should use `##` and be sentence case.

Use *italics* for filenames and for names of columns/fields, e.g. *basisOfRecord*.

Enclose references to sample values in double quptation marks `"..."`, e.g. "PreservedSpecimen".

Use *italics* and carrots for file paths as well as navigation paths, e.g. *My Profile > Occurrence Management > Administration Control Panel* or *Sitemap > Additional Resources > Glossary*.

Use **bold** for emphasis, e.g. "After making an edit, **remember to save**".

Format code snippets with \`...\`, e.g. `bundle exec jekyll serve`.

File extensions written as part of a filename are lowercase, e.g. *example.jpg*, but when written alone are uppercase, e.g. "the file should be a JPG."

Introduce the topic on a page using classes, e.g.
```
{{< notice info >}}
  This Symbiota Docs page is about...
{{</ notice >}}
```
Or add tips:
```
{{< notice tip >}}
  Here's a tip about this feature...
{{</ notice >}}
```

## Including media in documentation pages

To include a basic image with a caption, do so e.g.:
```
{% include figure image_path="/assets/images/lacmip-logo.jpg" alt="alt text goes here" caption="Figure caption text goes here." %}
```

To include a basic image without a caption, do so e.g.:
```
<img src="{{ site.baseurl }}/assets/images/access_login.png" alt="" width="100"/>{: .align-right}
```

To include a video, do so e.g.:
```
{% include video id="XsxDH4HcOWA" provider="youtube" %}
```

## Page-level options

There are several things you may wish to control at the page level by overwriting site defaults. These include...
- remove the right-hand table of contents by including `toc: false` to the yml header of the page
- create new headers by preceeding text on a new line with `#`; first- (`#`) and second-tier (`##`) headers will index in sidebar navigation

## Naming files

Markdown files being added to the *_documentation* collection should be named descriptively yet succinctly. Do not use any character other than a-z.

Image files should be named descriptively. Recommendation is to name them according to the page they are being linked to, e.g. *labels_designs.jpg* is linked to the labels page.

## Other helpful resources
- [GitHub Formatting Syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Markdown Emojis Directory](https://gist.github.com/rxaviers/7360908)
