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
  <div v-for="expense in list">
    <p> {{ expense.date }} | {{ expense.amout }}</p>
    <p>{{ expense.description }}</p>
  </div>
</template>

<style lang="stylus">

</style>
