<template>
  <div class="title-div">
    <div id="title">
      <slot>标题</slot>
    </div>
    <div class="line"></div>
  </div>

</template>

<script>
  export default {
    name: "Title"
  }
</script>

<style scoped lang="scss">
  $color: #4E7282;
  .title-div {
    display: flex;

    margin: 10px 10px;
    padding: 5px 0;
    #title {
      width: 100px;
      padding-left: 30px;
      background-color: $color;
      color: white;
    }
    .line {
      border-bottom: $color 1px solid;
      width: 90%;
    }
  }

</style>