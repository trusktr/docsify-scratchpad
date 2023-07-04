# This is a test

The following is a Lume scene with a box:

<div style="width: 400px; height: 300px;">
  <lume-scene webgl>
    <lume-point-light color="white" position="0 0 500"></lume-point-light>
    <lume-box size="100 100 100" align-point="0.5 0.5 0.5" mount-point="0.5 0.5 0.5" color="royalblue" rotation="10 20 30"></lume-box>
  </lume-scene>
</div>
<script type="module">
  const resp = await fetch('https://unpkg.com/lume@0.3.0-alpha.26/dist/global.js')
  const code = await resp.text()
  const script = document.createElement('script')
  script.textContent = code
  document.head.append(script)
  // await new Promise(r => script.onload = r)
  const {defineElements} = LUME
  defineElements()
</script>
