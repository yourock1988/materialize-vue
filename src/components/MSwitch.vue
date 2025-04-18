<script>
export default {
  // props: {
  //   checked: {
  //     type: Boolean,
  //     default: false,
  //   },
  //   disabled: {
  //     type: Boolean,
  //     default: false,
  //   },
  // },
  props: ['disabled', 'isUserReady'],
  emits: ['update:isUserReady'],
  data() {
    return {}
  },
}
</script>
<template>
  <!-- Switch -->
  <div class="switch">
    <label>
      Off
      <input
        :checked="isUserReady"
        type="checkbox"
        @change="$emit('update:checked', $event.target.checked)"
        :disabled="disabled"
      />
      <span class="lever"></span>
      On
    </label>
  </div>

  <!-- Disabled Switch -->
  <!-- <div class="switch">
    <label>
      Off
      <input disabled type="checkbox" />
      <span class="lever"></span>
      On
    </label>
  </div> -->
</template>
