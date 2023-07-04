# This is a test

The following is a Lume scene with a box:

<div style="width: 400px; height: 300px;">
  <lume-scene webgl>
    <lume-point-light color="white" position="-500 -500 500"></lume-point-light>
    <lume-box id="box" size="100 100 100" color="royalblue" rotation="10 20 30"></lume-box>
    <lume-camera-rig initial-distance="200" min-distance="100" max-distance="800"></lume-camera-rig>
  </lume-scene>
</div>
<script>
  (async function() {
    const resp = await fetch('https://unpkg.com/lume@0.3.0-alpha.26/dist/global.js')
    const code = await resp.text()
    const script = document.createElement('script')
    script.textContent = code
    document.head.append(script)
    const {defineElements} = LUME
    defineElements()
    const box = document.querySelector('#box')
    box.rotation = (x, y, z) => [x, y+0.2, z+0.2]
  })()
</script>
