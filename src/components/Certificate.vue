<template>
  <div>
    <Title>
      荣誉证书
    </Title>
    <Content :List="certificateOfHonor"/>
  </div>
</template>

<script>
  import Title from './components/Title'
  import Content from './components/Content'

  import {certificateOfHonor} from '@/common/data'
  export default {
    name: "Certificate",
    components: {
      Title,
      Content
    },
    data() {
      return {
        certificateOfHonor,
      }
    }
  }
</script>

<style scoped lang="scss">

</style>