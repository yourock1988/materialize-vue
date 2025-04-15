<script>
import MButton from './components/MButton.vue'
import MInputText from './components/MInputText.vue'

export default {
  components: { MButton, MInputText },

  data() {
    return {
      message: '',
    }
  },
}
</script>
<template>
  <section>
    <article>
      <MButton caption="Войти" />
    </article>
    <article>
      <MInputText v-model="message" placeholder="Введите ваше" />
    </article>
  </section>
</template>
