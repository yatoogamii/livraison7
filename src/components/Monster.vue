<template>
  <div class="monster-container">
      <h2 class="user-container__name">Monster</h2>
    <div class="monster-container__life-bar" :style="{width: hpMonster + '%'}">
      <h2 class="monster-container__hp">{{hpMonster}}</h2>
    </div>
    <img v-if="winner == 'Monster' || hpMonster != 0" :src="idle" alt="monster character"/>
    <img  v-else :src="imgDeath" alt="monster character"/>
  </div>
</template>

<script>
  export default{
    name: 'Monster',
    props: ['hpMonster', 'winner', 'death'],
    data() {
      return {
        idle: require('./../assets/img/monster-idle.gif'),
        imgDeath: require('./../assets/img/monster-death.gif')
      };
    }
    
  }
</script>

<style lang="scss" scoped>
.monster-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  .monster-container__life-bar {
    position: relative;
    background-color: #4caf50;
    margin-right: auto;
    height: 3rem;
    .monster-container__hp {
      position: absolute;
      left: 14.4rem;
      top: 0.7rem;
    }
  }
  .user-container__name {
    margin-bottom: 1rem;
  }
}

</style>

