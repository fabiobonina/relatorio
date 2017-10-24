<script>
export default {
  computed: {
    list () {
      return this.$store.state.Expenses.list
    }
  }
}
</script>

<template>
  <div>
    <div class="expense" v-for="expense in list">
    <p>{{ expense.date }} | {{ expense.amount }}</p>
    <p>{{ expense.descrisotion }}</p>
  </div>
  </div>
  
</template>

<style>
  .expense {
    border-bottom:
  }
</style>
