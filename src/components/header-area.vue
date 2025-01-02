<template>
       <div class="header-area">
         <h2>{{ title }}</h2>
         <div class="subtitle">{{ subtitle }}</div>
       </div> 
</template>

<script setup>
const props = defineProps({
    title:{
        type: String,
        default:() => {}
    },
    subtitle:{
        type: String,
        default: () => {}
    }
})
</script>

<style lang="less" scoped>
.header-area{
    height: 84px;
    
  .subtitle{
    margin-top: 8px;
  }
}
</style>   