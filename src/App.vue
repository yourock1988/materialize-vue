<script>
import MButton from './components/MButton.vue'
import MInputText from './components/MInputText.vue'
import MFAB from './components/MFAB.vue'
import SwitchesCheckbox from './components/SwitchesCheckbox.vue'

export default {
  components: { MButton, MInputText, MFAB, SwitchesCheckbox },

  data() {
    return {
      message: '',
      isShowFAB: false,
      hasPulseFAB: false,
      checked: false,
      isDisabled: false,
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
        :caption="checked ? 'ON' : 'OFF'"
        @click="checked = !checked"
        :is-toggle="!checked"
      />
      <MButton
        :caption="isDisabled ? 'Enable' : 'Disable'"
        @click="isDisabled = !isDisabled"
        :is-toggle="isDisabled"
      />
    </article>

    <article>
      <SwitchesCheckbox v-model:checked="checked" :disabled="isDisabled" />
    </article>
  </section>
</template>
