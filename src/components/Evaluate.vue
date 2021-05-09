<template>
  <div>
    <Title>
      自我评价
    </Title>
    <div class="content">
      <div>{{selfEvaluation}}</div>
    </div>
  </div>
</template>

<script>
  import Title from './components/Title'

  import {selfEvaluation} from '@/common/data'
  export default {
    name: "Evaluate",
    components: {
      Title,
    },
    data() {
      return {
        selfEvaluation,
      }
    }
  }
</script>

<style scoped lang="scss">
  .content {
    padding-left: 50px;
    font-weight: bold;
    div {
      padding: 3px 0px;
    }
  }
</style>