<template>
  <div>
    <Title>
      项目经验
    </Title>
    <div class="content">
      <experience-item></experience-item>
    </div>

  </div>
</template>

<script>
  import Title from './components/Title'
  import ExperienceItem from './components/ExperienceItem'
  export default {
    name: "Experience",
    components: {
      Title,
      ExperienceItem
    }
  }
</script>

<style scoped>
  .content {
    padding-left: 50px;
    width: 90%;
  }
</style>