<template>
  <div class="history">
    <HeaderComponent/>

    <section class="items">
      <button class="green_button">
          + Nova transação
      </button>
      <FiltersComponent/>

      <div class="items_title">
        <span></span>
        <h3>Todas as transações</h3>
        <span></span>
      </div>

      <div class="list_transactions">
        <TransactionItem v-for="(item, index) in transactionList" :key="index" :transactionObject="item"/>
      </div>
    </section>
  </div>
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue'
import FiltersComponent from '../components/FiltersComponent.vue'
import TransactionItem from '../components/TransactionItem.vue'
import TransactionItems from '../fridge_transactions.json'

export default {
  name: "HistoryView",
  components: { HeaderComponent, FiltersComponent, TransactionItem },
  data: () => {
    return {
      date: new Date(),
      transactionList: TransactionItems
    }
  },
  methods: {
  }
}

</script>

<style lang="scss" scoped>
  .history {
    display: flex;
    justify-content: center;

    .list_transactions {
      padding: 0px 8vw 0px 12vw;
      overflow-y: scroll;
    }
  }
</style>

