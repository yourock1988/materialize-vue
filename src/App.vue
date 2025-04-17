<script>
import MButton from './components/MButton.vue'
import MInputText from './components/MInputText.vue'
import MFAB from './components/MFAB.vue'

export default {
  components: { MButton, MInputText, MFAB },

  data() {
    return {
      message: '',
      isShowFAB: false,
      hasPulseFAB: false,
    }
  },
}
</script>

<template>
  <section>
    <article>
      <MButton
        caption="isShowFAB"
        :is-toggle="isShowFAB"
        @click="isShowFAB = !isShowFAB"
      />
      <MButton
        caption="hasPulseFAB"
        :is-toggle="hasPulseFAB"
        @click="hasPulseFAB = !hasPulseFAB"
      />
    </article>

    <article>
      <MInputText v-model="message" placeholder="Введите ваше" />
    </article>

    <article>
      <MFAB :isShow="isShowFAB" :hasPulse="hasPulseFAB" mui-icon="home" />
    </article>
  </section>
</template>
