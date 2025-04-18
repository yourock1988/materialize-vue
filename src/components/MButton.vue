<script>
export default {
  props: {
    caption: {
      type: String,
      default: 'Отправить',
    },
    isToggle: {
      type: Boolean,
      default: false,
    },
    isShowIcon: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<template>
  <a class="waves-effect waves-light btn">
    <i v-if="isShowIcon" class="material-icons left">{{
      isToggle ? 'remove' : 'add'
    }}</i>
    <span>{{ caption }}</span>
  </a>
</template>

<style>
a {
  margin: 0 5px;
}
</style>
