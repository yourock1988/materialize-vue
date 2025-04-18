<script>
import MButton from './components/MButton.vue'
import MInputText from './components/MInputText.vue'
import MFAB from './components/MFAB.vue'
import MSwitch from './components/MSwitch.vue'
import MSlider from './components/MSlider.vue'

export default {
  components: { MButton, MInputText, MFAB, MSwitch, MSlider },

  data() {
    return {}
  },
}
</script>

<template>
  <section>
    <article>
      <MSlider />
    </article>
  </section>
</template>
