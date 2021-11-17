<!-- 
To create a topic inside a section, use the following instructions:
1. Create directory inside `content/<section name>`, named after the desired topic
2. Create files corresponding to each language, named like so:
  - `_index.<2-letter language tag>.md`
3. Insert the frontmatter below in the file
4. Add text content below the frontmatter (template includes example content)
5. Structure inner content in directories and content pages (use `content-page-template.md`)
  - date: creation date
  - lastmod: last date of content update
  - weight: optional, placement in list of topics
  - draft: false/true, if true page won't be published right away
  - keywords: ["term1", "term2"] -- will work in the search 
 -->
---
title: "How to pay your bill"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 3
draft: false
authors: ["Charles Darwin"]
editors: ["Sybylla Merian"]
translators: ["Princess Therese of Bavaria"]
keywords: ["template","markdown"]
---

Musce libero nunc, dignissim quis turpis quis, semper vehicula dolor. Suspendisse tincidunt consequat quam, ac posuere leo dapibus id. Cras fringilla convallis elit, at eleifend mi interam.

{{< notice note >}}
  This is a simple note.
{{</ notice >}}

{{< notice tip >}}
  This is a simple tip.
{{</ notice >}}

{{< notice info >}}
  This is a simple info.
{{</ notice >}}

{{< button href="http://mylink.com" text="Click here to go to my link" >}}

{{< tabs >}}
  {{< tab "first" >}}
   This is first tab
  {{</ tab >}}

  {{< tab "second" >}}
  this is second tab
  {{</ tab >}}

  {{< tab "third" >}}
  this is third tab
  {{</ tab >}}
{{</ tabs >}}

#### Darwin Core Definition
{{< dwc-term id="catalogNumber" verbatim="Catalog Number" descr="The unique identifier (primary key) for the specimen record. This field should be used to store the barcode or the accession number (herbaria only). This field is enforced to be unique per collection." ex="WIS-L-0123456, ASU0012345, 12345" dwc="catalogNumber" >}}

Nulla non sollicitudin. Morbi sit amet laoreet ipsum, vel pretium mi. Morbi varius, tellus in accumsan blandit, elit ligula eleifend velit, luctus mattis ante nulla condimentum nulla. Etiam vestibulum risus vel arcu elementum eleifend. Cras at dolor eget urna varius faucibus tempus in elit.

### Image Example

Nunc porta malesuada porta. Etiam tristique vestibulum dolor at ultricies. Proin hendrerit sapien sed erat fermentum, at commodo velit consectetur.

![image example](/symbiota-docs/images/banner.jpg "image")

Etiam vestibulum risus vel arcu elementum eleifend. Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet, tempus metus quis, pharetra turpis. Phasellus at massa sit amet ante semper fermentum sed eget lectus. Quisque id dictum magna, et dapibus turpis.

### Example Of Code Block

In accumsan lacus ac neque maximus dictum. Phasellus eleifend leo id mattis bibendum. Curabitur et purus turpis. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae;

```html
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="/assets/css/main.css">
  <link rel="shortcut icon" type="image/png" href="/assets/img/favicon.png" >
  <script src="/assets/js/main.js"></script>
</head>
```

### Text and Quote

Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet, tempus metus quis, pharetra turpis. Phasellus at massa sit amet ante semper fermentum sed eget lectus. Quisque id dictum magna turpis.

> Etiam vestibulum risus vel arcu elementum eleifend. Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet

Etiam vestibulum risus vel arcu elementum eleifend. Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet, tempus metus quis, pharetra turpis. Phasellus at massa sit amet ante semper fermentum sed eget lectus. Quisque id dictum magna, et dapibus turpis.Etiam vestibulum risus vel arcu elementum eleifend. Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet, tempus metus quis, pharetra turpis. Phasellus at massa sit amet ante semper fermentum sed eget lectus. Quisque id dictum magna, et dapibus turpis.

## Youtube

The video id has to be added inside the shortcode:

{{< youtube QAsypzpY-aA >}}

## Gist

{{< gist johndoe 12345 >}}