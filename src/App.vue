<script>
import MButton from './components/MButton.vue'
import MInputText from './components/MInputText.vue'
import MFAB from './components/MFAB.vue'
import MSwitch from './components/MSwitch.vue'
import MSlider from './components/MSlider.vue'
import MmultipleSelect from './components/MmultipleSelect.vue'

export default {
  components: { MButton, MInputText, MFAB, MSwitch, MSlider, MmultipleSelect },

  data() {
    return {
      selected: [],
    }
  },
}
</script>

<template>
  <section>
    <!-- <article>
      <MSlider />
    </article> -->
    <article>
      <MmultipleSelect />
    </article>
  </section>
</template>
