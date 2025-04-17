<script>
export default {
  props: ['caption', 'isToggle'],
}
</script>

<template>
  <a class="waves-effect waves-light btn">
    <i class="material-icons left">{{ isToggle ? 'remove' : 'add' }}</i>
    <span>{{ caption }}</span>
  </a>
</template>

<style>
a {
  margin: 0 5px;
}
</style>
