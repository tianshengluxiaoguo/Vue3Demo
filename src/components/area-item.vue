<template>
    <div class="area-item">
        <div class="item-ineer">
            <!-- 1.图片 -->
            <div class="cover">
                <img :src="itemDate.picture_url" alt="">
            </div>
            <div class="info">
                <!-- 2.信息 -->
                 <div class="title">
                    {{ itemDate.id }}
                 </div>
                 <div class="name">
                    {{ itemDate.name }}
                 </div>
                 <div class="price_format">
                    {{ itemDate.price_format + '/晚' }}
                 </div>
                 <div class="bottom_info">
                    {{ itemDate.bottom_info.content }}
                 </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
    itemDate: {
        type: Object,
        default:() => {}
    }
})
</script>

<style lang="less" scoped>
.area-item{
    width: 33.333333%;

    .item-ineer{
      margin: 0 8px 12px;
      color: #484848;
      font-weight: 800;

      img {
        width: 100%;
        border-radius: 20px;
      }

      .info{
        .title{
            margin-top: 8px;
            font-size: 12px;
        }
      }
    }
}
</style>