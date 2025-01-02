<template>
    <div class="app">
      <HeaderArea :title="highScore.title" :subtitle="highScore.subtitle"></HeaderArea>

     <div class="room-list">
        <template v-for="item in highScore.list" :key="item.id">
        <AreaItem :itemDate="item">
          
        </AreaItem>
      </template>
     </div>
    </div>
</template>

<script setup>
// 1.获取数据
import highScore from './data/high_score.json'
import HeaderArea from './components/header-area.vue'
import AreaItem from './components/area-item.vue'
</script>

<style lang="less" scoped>
.app{

    width: 1025px;
    margin: 100px auto;
}

.room-list{
    display: flex;
    flex-wrap: wrap;
     
}
</style>