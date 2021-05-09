<template>
  <div class="content">
    <div v-for="(item, index) in List" :key="index" class="item">
      <span class="option">{{item.key}}</span><span>{{item.value}}</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Content",
    props: {
      List: {
        type: Array,
        default() {
          return []
        }
      }
    }
  }
</script>

<style scoped lang="scss">
  .content {
    padding-left: 50px;
    .item {
      padding: 3px 0px;
      line-height: 30px;
      .option {
        font-weight: bold;
      }
    }
  }
</style>