<script>
export default {
  props: {
    checked: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  emits: ['update:checked'],
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
        :checked="checked"
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
