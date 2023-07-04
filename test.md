# Load a Lume scene

LoadView this page in Docsify-This to see it rendered:

https://docsify-this.net/?executeScript=true&basePath=https://raw.githubusercontent.com/trusktr/tmp/main&homepage=test.md#/

The following is a [Lume](https://lume.io) scene with a rotating box:

<div style="width: 400px; height: 300px;">
  <lume-scene webgl>
    <lume-box id="box" size="100 100 100" mount-point="0.5 0.5 0.5" color="royalblue" rotation="10 20 30"></lume-box>
    <lume-camera-rig initial-distance="500" min-distance="100" max-distance="1200">
      <lume-point-light color="white" position="-500 -500 500"></lume-point-light>
    </lume-camera-rig>
  </lume-scene>
</div>

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
