<template>
  <div class="plan">
    <Plan
      v-for="plan in plans"
      :name="plan" :key="plan"
      @select="selectPlan"
      :selected-plan="selectedPlan"
    />
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
    plans: ['The Hacker', 'The Single', 'The Curious', 'The Addict'],
    selectedPlan: null
  }),
  methods: {
    selectPlan(plan) {
      this.selectedPlan = plan
    }
  }
}
</script>

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
