<script>
import { QDatetime } from 'quasar'
  export default {
    components: { QDatetime },

    data () {
      return {
        expense: {
          amount: '',
          descrisotion: '',
          date: new Date()
        }
      }
    },
    methods: {
      submit () {
        const cloned = JSON.parse(JSON.stringify(this.expense))
        this.$store.commit('ADD_EXPENSE', cloned)
        this.reset()
      },
      reset () {
        this.expense.amount = ''
        this.expense.descrisotion = ''
        this.expense.date = new Date()
        this.$refs.amount.focus()
      }
    }
  }
</script>

<template>
  <form @submit.prevent="submit">
    <input ref="amount" class="my-input" type="number" v-model="expense.amount" placeholder="R$">
    <input class="my-input" type="text" v-model="expense.descrisotion" placeholder="Descrição">
    <input class="my-input" type="date" v-model="expense.date" placeholder="Data">
    <q-datetime type="date" v-model="expense.date" color="amber" stack-label="No 'Clear' button" no-clear/>
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
