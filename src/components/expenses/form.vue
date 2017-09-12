<script>
  export default {

    data () {
      return {
        expenses: {
          amount: '',
          descrisotion: '',
          date: ''
        }
      }
    },
    methods: {
      submit () {
        
      }
    }
  }

</script>

<template>
  <form @submit.prevent="submit">
    <input class="my-input" type="number" v-model="expenses.amount" placeholder="R$">
    <input class="my-input" type="text" v-model="expenses.descrisotion" placeholder="Descrição">
    <input class="my-input" type="text" v-model="expenses.date" placeholder="Data">
    <button class="primary my-button">Salvar</button>
  </form>
</template>

<style scoped>
  .my-input {
    width: 100%;
    margin-bottom: 20px;
  }

  .my-button {
    width: 100%;
  }
</style>
