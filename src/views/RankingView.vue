<template>
  <div class="ranking">
    <HeaderComponent/>

    <section class="items">
      <div class="items_title">
        <span></span>
        <h3>Mais consumidos</h3>
        <span></span>
      </div>

      <div class="list_ranking">
        <RankingItem v-for="(item, index) in orderedList" :key="index" :rankingObject="item" :position="index+1"/>
      </div>
    </section>
  </div>
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue'
import RankingItem from '../components/RankingItem.vue'
import RankingItems from '../fridge_consumption_stats.json'

export default {
  name: "RankingView",
  components: { HeaderComponent, RankingItem },
  data: () => {
    return {
      rankingList: RankingItems,
      orderedList: []
    }
  },
  methods: {
    orderByHighestConsumption() {
      this.orderedList = this.rankingList.sort(
        (a, b) => (a.totalConsumption - b.totalConsumption)
      );
    }
  },
  beforeMount() {
    this.orderByHighestConsumption();
  }
}

</script>

<style lang="scss" scoped>
  .ranking {
    display: flex;
    justify-content: center;

    .items_title {
      margin-top: 36px;
      margin-bottom: 37px;
    }

    .list_ranking {
      padding:24px 16px 0px 48px;
      overflow-y: scroll;
      margin-top: -18px;
    }
  }
</style>
