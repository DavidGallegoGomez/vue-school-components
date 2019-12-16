<template>
  <div @click="select" class="plan" :class="{'active-plan': isSelected}">
    <div class="description">
      <br>
      <span class="title">
        {{ name }}
      </span>
      <br>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Plan',
  props: {
    name: {
      type: String,
      default: 'The Default',
      required: true
    },
    selectedPlan: { type: String }
  },
  computed: {
    isSelected() {
      return this.name === this.selectedPlan
    }
  },
  /* data: () => ({
    selected: false
  }), */
  methods: {
    select() {
      this.$emit('select', this.name)
      // this.selected = true
    }
  }
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
.active-plan {
  background-color: blueviolet
}
</style>
