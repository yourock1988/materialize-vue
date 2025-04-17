<script>
export default {
  props: ['isShow', 'hasPulse', 'muiIcon'],

  data() {
    return {
      hasScaleOut: true,
    }
  },

  watch: {
    isShow(newValue) {
      this.hasScaleOut = !newValue
    },
  },

  mounted() {
    requestAnimationFrame(() => {
      if (this.isShow) this.hasScaleOut = false
    })
  },
}
</script>

<template>
  <a
    ref="elA"
    class="waves-effect waves-light btn-floating btn-large scale-transition"
    :class="{ 'scale-out': hasScaleOut, pulse: hasPulse }"
  >
    <i class="material-icons">{{ muiIcon }}</i>
  </a>
</template>
