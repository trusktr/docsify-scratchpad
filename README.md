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
> Learn more about [Markdown format](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

Any of the content on this page can be viewed online using a Docsify-powered site. [Docsify-This](https://docsify-this.net) is a static Docsify site that specializes in rendering Markdown files that you give it via URL query parameters. The whole thing is all static (meaning there is no backend, it is just statically-served files), and it fetches and renders your desired Markdown page on the fly with Docsify. For example, you can view this repo like so:

...

# Markdown Extras

Docsify adds a few additional features to the Markdown format ([for example](https://docsify.js.org/#/helpers)). It also supports `<style>` and `<script>` tags, allowing dynamic possibilities with our Markdown output.
