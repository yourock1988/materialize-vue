<script>
import 'materialize-css/extras/noUiSlider/nouislider.css'

import noUiSlider from 'materialize-css/extras/noUiSlider/nouislider.js'

export default {
  mounted() {
    const options = {
      start: [20, 80],
      connect: true,
      step: 1,
      orientation: 'horizontal', 
      range: {
        min: 0,
        max: 100,
      },
    }

    requestAnimationFrame(() => {
      noUiSlider.create(this.$refs.elSlider, options)
      M.AutoInit()
    })
  },
}
</script>
<template>
    <p class="range-field scrollspy">
      <input type="range" id="test5" min="0" max="100" />
      <div id="range-input" class="range-field" ref="elSlider"></div>
    </p>
    <div id="range-input" class="noUi-target noUi-ltr noUi-horizontal"><div class="noUi-base"><div class="noUi-origin" style="left: 20%;"><div class="noUi-handle noUi-handle-lower" data-handle="0" style="z-index: 5;"><div class="noUi-handle-touch-area"></div><div class="noUi-tooltip"><span>20</span></div></div></div><div class="noUi-connect" style="left: 20%; right: 20%;"></div><div class="noUi-origin" style="left: 80%;"><div class="noUi-handle noUi-handle-upper" data-handle="1" style="z-index: 4;"><div class="noUi-handle-touch-area"></div><div class="noUi-tooltip"><span>80</span></div></div></div></div></div>
</template>
