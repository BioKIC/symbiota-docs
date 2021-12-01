---
title: "How to run a local version of Symbiota Docs"
date: 2021-12-01
lastmod: 2021-12-01
weight: 1
draft: false
authors: ["Laura Rocha Prado"]
keywords: ["contribute", "develop", "hugo", "local", "documentation"]
---

You can run the Symbiota Docs website in your own computer if you'd like to contribute with content and you're interested in previewing changes before pushing them to us, or for development purposes as well, in case you'd like to suggest theme modifications.

Symbiota Docs is a static documentation website compiled with Hugo. The files that create each page and topic are written in [Markdown](https://en.wikipedia.org/wiki/Markdown) (with the possibility to add some [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)), and "translated" by Hugo into static HTML files. 

In a nutshell, what you need to run a local version of the Symbiota Docs website is:
1. Install Hugo in your computer
2. Download or clone the [symbiota docs GitHub repository](https://github.com/biokic/symbiota-docs)
3. Run a Hugo server
4. Enjoy!

## Install Hugo

[Hugo](https://gohugo.io/) is a framework for building static websites. To install Hugo, please visit the [official Hugo installation documentation](https://gohugo.io/getting-started/installing/).

## Get the Symbiota Docs files

1. Visit the [Symbiota Docs GitHub repository](https://github.com/biokic/symbiota-docs).
2. Click the "Code" button on the right side of the page.
3. Select the option your most comfortable with (clone, open with GitHub desktop or download zip).
4. Go to the folder where you have placed your downloaded files. If you have a zipped archive, unzip it.
5. Open a terminal/shell/command-line tool in your operating system and navigate to your folder (in the example below my files are in the Documents directory, inside another directory called symbiota-docs):

{{< highlight batchfile >}}
cd Documents/symbiota-docs/
{{< /highlight >}}

6. Run a development Hugo server with the following command in the same command-line tool:

{{< highlight batchfile >}}
hugo server -D
{{< /highlight >}}

7. If your website doesn't pop up automatically, in a browser, navigate to the address indicated by your terminal (normally it's `http://localhost:1313/` or some similar with different port numbers).
8. You are now live locally! To make changes, open the desired file (ending in `.md` for Markdown) in a text editor, make changes and save to see the modifications instantly reflected in your local website.