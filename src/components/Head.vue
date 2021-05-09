<template>
  <div class="head">
    <div id="title">个人简历</div>
    <div class="strip">
      <strip :height="30" :width="560" direction="right" color="#4E7282" big="bottom"/>
      <strip :height="20" :width="412" direction="left" color="#C19F67" big="top" class="second-strip"/>
    </div>

  </div>
</template>

<script>
  import Strip from './components/Strip'
  export default {
    name: "Head",
    components: {
      Strip
    }
  }
</script>

<style scoped lang="scss">
  $color: #4E7182;
  .head {
    #title {
      color: $color;
      font-size: 36px;
      border-right: solid 2px $color;
      width: 15%;
      padding: 5px 0;
      margin-bottom: 10px;
     }
    .strip {
      display: flex;
      justify-content: space-between;
      .second-strip {
        position: relative;
        right: 10px;
        padding-top: 10px;
        margin-right: 0;
      }
    }
  }
</style>