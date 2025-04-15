<script>
export default {
  props: ['modelValue', 'placeholder'],

  emits: ['update:model-value'],
}
</script>

<template>
  <div>
    <div class="input-field">
      <input
        :placeholder="placeholder"
        id="first_name"
        type="text"
        class="validate"
        :value="modelValue"
        @input="$emit('update:model-value', $event.target.value)"
      />
      <label for="first_name" :class="{ active: !!placeholder }"
        >First Name</label
      >
    </div>
  </div>
</template>
