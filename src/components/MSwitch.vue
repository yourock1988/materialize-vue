<script>
export default {
  props: {
    modelValue: {
      type: Boolean,
      default: false,
    },
    isDisabled: {
      type: Boolean,
      default: false,
    },
    caption: {
      type: String,
      default: 'Off',
    },
  },

  emits: ['update:model-value'],
}
</script>

<template>
  <div class="switch">
    <label>
      <input
        type="checkbox"
        :checked="modelValue"
        :disabled="isDisabled"
        @change="$emit('update:model-value', $event.target.checked)"
      />
      <span class="lever"></span>
      {{ caption }}
    </label>
  </div>
</template>
