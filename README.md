# docsify-scratchpad

This repo is entirely Markdown files compatible with [Docsify](https://docsify.js.org), a tool for rendering sites and pages written in Markdown, without any build tools or command line.

> **Note** Markdown is (essentially) a superset of HTML. While Markdown files can contain HTML, Markdown code allows writing shortcuts for otherwise more-verbose HTML. The rendered output of a Markdown file then contains HTML generated from the shorter code. For example, writing this,
>
> ```md
> # Hello
> ```
> 
> results in an HTML heading element `<h1>Hello</h1>` being created, and the result looks like this:
> 
> > # Hello
> 
> Learn more about the [Markdown format](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

Any of the content on this page can be viewed online using a Docsify-powered site. [Docsify-This](https://docsify-this.net) is a static Docsify site that specializes in rendering Markdown files that you give it via URL query parameters. The whole thing is all static (meaning there is no backend, it is just statically-served files), and it fetches and renders your desired Markdown page on the fly with Docsify.

For example, you can view this repo like so:

https://docsify-this.net/?basePath=https://raw.githubusercontent.com/trusktr/docsify-scratchpad/main&homepage=README.md&executeScript=true&toc=true&browser-tab-title=docsify-scratchpad&edit-link=https://github.com/trusktr/docsify-scratchpad/blob/main/README.md&toc-headings=h1,h2#/?id=markdown-extras

The options in the URL are created from the options chosen in the Docsify-This UI before hitting the publish button.

# Markdown Extras

Docsify adds a few additional features to the Markdown format ([for example](https://docsify.js.org/#/helpers)).

Docsify also supports `<style>` and `<script>` tags, allowing dynamic possibilities with our Markdown output.

## Styling

Here's a style example. The previous heading is colored due to this Markdown file containing the following `<style>` tag with [CSS style code](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) inside of it:

```html
<style>
  #styling {
    background: deeppink;
  }
</style>
```

<style>
  #styling {
    background: deeppink;
  }
</style>
