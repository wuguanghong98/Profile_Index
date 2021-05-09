<template>
  <div class="skill-div">
    <Title class="title">
      专业技能
    </Title>
    <Content :List="skill"/>
  </div>
</template>

<script>
  import Title from './components/Title'
  import Content from './components/Content'

  import {skill} from '@/common/data'
  export default {
    name: "Skill",
    components: {
      Title,
      Content
    },
    data() {
      return {
        skill,
      }
    }
  }
</script>

<style scoped lang="scss">

</style>