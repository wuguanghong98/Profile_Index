<template>
  <div>
    <el-table
            :data="projects"
            border
            style="width: 100%">
      <el-table-column
              prop="projectName"
              label="项目名称"
              width="180">
      </el-table-column>
      <el-table-column
              prop="projectAddress"
              label="项目地址"
              width="380">
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
  import {projects} from '@/common/data'
  export default {
    name: "ExperienceItem",
    data() {
      return {
        projects
      }
    }
  }
</script>

<style scoped lang="scss">

</style>