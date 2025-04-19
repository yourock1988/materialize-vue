<script>
export default {
  data() {
    return {
      caption: 'Выберите город',
      options: [{ kyiv: 'Киев' }],
    }
  },

  mounted() {
    console.log(M)
    const instance = M.FormSelect.init(this.$refs.elSelect)
    console.log(instance)
    instance.dropdown.options.onOpenStart = () => console.log('yo!')
    instance.dropdown.options.onCloseStart = () => console.log('unyo!')

    setInterval(() => {
      console.log(instance.dropdown.isOpen)
      // instance.open()
    }, 1000)
  },
}
</script>

<template>
  <div class="multiply-select-backdrop">
    <div class="input-field col s12">
      <select ref="elSelect" multiple>
        <option value="" disabled>Choose your option</option>
        <option value="kyiv">Киев</option>
        <option value="kharriv">Харьков</option>
        <option value="odesa">Одесса</option>
      </select>
      <label>Materialize Multiple Select</label>
    </div>
  </div>
</template>

<style>
.backdrop {
}

.input-field {
  max-width: 50%;
  margin: 0 auto;
}
</style>
