<template>
  <div id="app">
      <el-row>
        <el-col :span="16" :offset="4">
          <Head/>
          <base-info/>
          <skill/>
          <experience/>
          <certificate/>
          <evaluate/>
        </el-col>
      </el-row>
  </div>
</template>

<script>
  import Head from './components/Head'
  import BaseInfo from './components/BaseInfo'
  import Skill from './components/Skill'
  import Experience from './components/Experience'
  import Certificate from './components/Certificate'
  import Evaluate from './components/Evaluate'

export default {
  name: 'App',
  components: {
    Head,
    BaseInfo,
    Skill,
    Experience,
    Certificate,
    Evaluate
  },
}
</script>

<style lang="scss">
  body {
    font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
    background-color: #ECF5FF;
    color: #606266;
    font-size:17px;
    #app {

    }
  }
</style>
