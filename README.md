# docsify-scratchpad

This repo is entirely Markdown files compatible with [Docsify](https://docsify.js.org), a tool for rendering sites and pages written in Markdown, without any build tools or command line.

We can use [Docsify-This](https://docsify-this.net) to create a shareable URL for viewing this rendering result of this page. Here's a URL created with Docsify-This (click it to view this page with _additional Markdown features not available if you're reading this on GitHub.com_):

> https://docsify-this.net/?basePath=https://raw.githubusercontent.com/trusktr/docsify-scratchpad/main&homepage=README.md&executeScript=true&toc=true&browser-tab-title=docsify-scratchpad&edit-link=https://github.com/trusktr/docsify-scratchpad/blob/main/README.md&toc-headings=h1,h2#/?id=markdown-extras

# Render Markdown from anywhere in your browser

Any of the content on this page can be viewed online using a Docsify-powered site.

[Docsify-This](https://docsify-this.net) is a static Docsify site that specializes in rendering Markdown files that you give it via URL query parameters (with added Markdown features of Docsify). It is a static site (meaning there is no backend, just statically-served files), and it fetches and renders your desired Markdown pages on the fly with Docsify.

In the above example URL, the options that appear after the `?` are created from the options chosen in the Docsify-This UI before hitting the publish button. If you [learn URL query parameter formatting](https://www.semrush.com/blog/url-parameters/), you can write or edit such URLs manually.

The raw Markdown code of this page can be viewed here:

https://raw.githubusercontent.com/trusktr/docsify-scratchpad/main/README.md

You can place this page you are reading into a docsify-this query parameter to specify which Markdown file it will render, by converting `https://raw.githubusercontent.com/trusktr/docsify-scratchpad/main/README.md` to `basePath=https://raw.githubusercontent.com/trusktr/docsify-scratchpad/main&homepage=README.md` and sticking that after the `?` in the URL.

# Self-hosted Docsify sites

If you'd like to host your site yourself, you can use Docsify directly to server your own static HTML page that loads Docsify and renders your statically-served Markdown files. A couple examples using Docsify for Markdown-based static websites are:

1. The Docsify site itself, https://docsify.js.org
2. [Lume](https://lume.io)'s documentation site, https://docs.lume.io

Docsify's [Showcase page](https://docsify.js.org/#/awesome?id=showcase) has more examples of self-hosted Docsify sites.

# Markdown Extras

Docsify adds a few additional features to the Markdown format ([for example](https://docsify.js.org/#/helpers)).

Docsify also supports `<style>` and `<script>` tags, allowing dynamic possibilities with our Markdown output.

## Styling

Here's a style example. The previous heading is colored due to this Markdown file containing the following `<style>` tag with [CSS style code](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) inside of it:

```html
<style>
  #styling {
    color: deeppink;
  }
</style>
```

<style>
  #styling {
    color: deeppink;
  }
</style>

## Scripts

Here's an example where render a 3D scene by writing Lume HTML, where we use a `<script>` like the following to load Lume's HTML elements.

```html
<div style="width: 400px; height: 300px;">
  <lume-scene webgl>
    <lume-box id="box" size="100 100 100" mount-point="0.5 0.5 0.5" color="royalblue" rotation="10 20 30"></lume-box>
    <lume-camera-rig initial-distance="500" min-distance="100" max-distance="1200">
      <lume-point-light color="white" position="-500 -500 500"></lume-point-light>
    </lume-camera-rig>
  </lume-scene>
</div>
<style>
  lume-scene { border: 1px solid deeppink; }
</style>

<script>
  async function loadScript(URL) {
    const response = await fetch(URL)
    const code = await response.text()
    const script = document.createElement('script')
    script.textContent = code
    document.head.append(script)
  }
  loadScript('https://unpkg.com/lume@0.3.0-alpha.26/dist/global.js').then(() => {
    const {defineElements} = LUME
    defineElements() // defines the Lume elements
    const box = document.getElementById('box') // get a reference to the <lume-box> element
    box.rotation = (x, y, z) => [x, y+0.2, z+0.2] // make it rotate
  })
</script>
```

Here's the result:

<div style="width: 400px; height: 300px;">
  <lume-scene webgl>
    <lume-box id="box" size="100 100 100" mount-point="0.5 0.5 0.5" color="royalblue" rotation="10 20 30"></lume-box>
    <lume-camera-rig initial-distance="500" min-distance="100" max-distance="1200">
      <lume-point-light color="white" position="-500 -500 500"></lume-point-light>
    </lume-camera-rig>
  </lume-scene>
</div>
<style>
  lume-scene { border: 1px solid deeppink; }
</style>

<script>
  async function loadScript(URL) {
    const response = await fetch(URL)
    const code = await response.text()
    const script = document.createElement('script')
    script.textContent = code
    document.head.append(script)
  }
  loadScript('https://unpkg.com/lume@0.3.0-alpha.26/dist/global.js').then(() => {
    const {defineElements} = LUME
    defineElements() // defines the Lume elements
    const box = document.getElementById('box') // get a reference to the <lume-box> element
    box.rotation = (x, y, z) => [x, y+0.2, z+0.2] // make it rotate
  })
</script>

> **Note** If you see a bunch of garbled non-sense in below this line, that is because you're reading this on GitHub, not in a Docsify site or with Docsify-This, and you should click the [first URL above](https://docsify-this.net/?basePath=https://raw.githubusercontent.com/trusktr/docsify-scratchpad/main&homepage=README.md&executeScript=true&toc=true&browser-tab-title=docsify-scratchpad&edit-link=https://github.com/trusktr/docsify-scratchpad/blob/main/README.md&toc-headings=h1,h2#/?id=markdown-extras) to view the rendered result.
