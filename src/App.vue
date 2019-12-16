<template>
  <div id="app">
    <ClickCounter />
    <br>
    <div class="content">
      <h1 class="title">Coffee Plans</h1>
      <h2 class="subtitle">We travel the world to source the very best single origin coffee for you</h2>
      <div class="plans">
        <plan-picker />
        <Plan name="Super"/>
      </div>
    </div>
  </div>
</template>

<script>
import ClickCounter from '@/components/ClickCounter.vue'
import PlanPicker from '@/components/PlanPicker.vue'
import Plan from '@/components/Plan.vue'

export default {
  name: 'app',
  components: {
    ClickCounter,
    PlanPicker,
    Plan
  } 
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
