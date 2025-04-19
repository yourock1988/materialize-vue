<script>
export default {
  mounted() {
    M.FormSelect.init(this.$refs.elSelect)
  },
}
</script>

<template>
  <div class="input-field col s12">
    <select ref="elSelect" multiple>
      <option value="" disabled>Choose your option</option>
      <option value="1">Option 1</option>
      <option value="2">Option 2</option>
      <option value="3">Option 3</option>
    </select>
    <label>Materialize Multiple Select</label>
  </div>
</template>
<style>
.input-field {
  max-width: 50%;
  margin: 0 auto;
}
</style>
