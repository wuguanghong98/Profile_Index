<template>
  <div>
    <Title>
      基本信息
    </Title>
    <div class="base-info">
      <div class="info-div" v-for="(item, index) in info" :key="index">
        <div class="item" v-for="(obj, indey) in item" :key="indey">
          <div class="option">{{obj.key}}</div><div class="choice">{{obj.value}}</div>
        </div>
      </div>
      <div class="info-div">
          <div class="block">
            <el-image
                    style="width: 200px; height: 200px"
                    :src="portrait"
                    :fit="fit"></el-image>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Title from './components/Title'

  import {info} from '@/common/data'

  export default {
    name: "BaseInfo",
    components: {
      Title
    },
    data() {
      return {
        info,
        portrait: require("@/assets/img/portrait.jpg"),
        fit: 'contain'
      }
    }
  }
</script>

<style scoped lang="scss">
  $border: 1px red solid;
  .base-info {
    display: flex;
    //border: $border;
    .info-div{
      //border: $border;
      flex: 1;
      padding: 0 0 0 50px;

      .item {
        display: flex;
        padding: 10px 2px;
        //border: $border;

        .option {
          font-weight: bold;
        }
        .choice {
          color: #606266;
        }
      }

      .block {
        padding: 5px 0;
      }
    }
  }
</style>