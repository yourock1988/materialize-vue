<script>
import MButton from './components/MButton.vue'
import MInputText from './components/MInputText.vue'
import MFAB from './components/MFAB.vue'
import MSwitch from './components/MSwitch.vue'

export default {
  components: { MButton, MInputText, MFAB, MSwitch },

  data() {
    return {
      message: '',
      isShowFAB: false,
      hasPulseFAB: false,
      checked: false,
      isDisabled: false,
      isUserReady: false,
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

    <article>
      <MButton
        :caption="checked ? 'IsON' : 'IsOFF'"
        @click="checked = !checked"
        :is-toggle="!checked"
      />
      <MButton
        :caption="'IsEnable'"
        @click="isUserReady = !isUserReady"
        :is-toggle="isDisabled"
      />
    </article>

    <article>
      <MSwitch v-model:isUserReady="isUserReady" :disabled="isDisabled" />
    </article>
  </section>
</template>
