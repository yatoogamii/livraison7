<template>
  <section class="container-button">
    <BtnAttack :dark="dark" :disabled="disabled" v-on:attack="$emit('attack')" class="container-button__btn-attack"></BtnAttack>
    <BtnSpeAttack :dark="dark"  :disabled="disabled"  v-on:spe-attack="$emit('spe-attack')" class="container-button__btn-spe-attack"></BtnSpeAttack>
    <BtnHeal :dark="dark"  :disabled="disabled"  v-on:heal="$emit('heal')" class="container-button__btn-heal"></BtnHeal>
    <BtnReset :dark="dark"  v-on:reset="$emit('reset')" class="container-button__btn-reset"></BtnReset>
  </section>
</template>

<script>

import BtnAttack from './BtnAttack.vue';
import BtnSpeAttack from './BtnSpeAttack.vue';
import BtnHeal from './BtnHeal.vue';
import BtnReset from './BtnReset.vue';

  export default{
    name: 'Skills',
    components: {
      BtnAttack,
      BtnSpeAttack,
      BtnHeal,
      BtnReset
    },
    props: ['disabled', 'dark']
  }
</script>

<style lang="scss" scoped>
.container-button {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>

