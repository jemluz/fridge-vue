<template>
    <div class="ranking_item">
        <div class="number">{{ position }}</div>
        <img class="image" :src="rankingObject.imageUrl" alt="">
        <div class="name">
            <h4>{{ rankingObject.name }}</h4>
            <p>{{ rankingObject.totalConsumption }} unidades consumidas</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'RankingItem',
    props: ['rankingObject', 'position']
}
</script>

<style lang="scss" scoped>
.ranking_item {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-bottom: 15px;

    .number {
        font-family: 'Quantico', sans-serif;
        font-size: 30px;
        color: #B8B8B8;
    }

    .image {
        height: 8vh;
        width: 8vh;
        margin-inline: 27px;
    }

    .name {
        h4 {
            font-family: 'Roboto', sans-serif;
            font-size: 16px;
        }

        p {
            font-size: 12px;
            color: #B8B8B8;
        }
    }
}
</style>