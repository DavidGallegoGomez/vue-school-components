<template>
  <div class="plan">
    <Plan v-for="plan in plans" :name="plan" :key="plan" />
  </div>
</template>

<script>
import Plan from '@/components/Plan.vue'

export default {
  name: 'PlanPicker',
  components: {
    Plan
  },
  data: () => ({
    plans: ['The Hacker', 'The Single', 'The Curious', 'The Addict']
  }) 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
