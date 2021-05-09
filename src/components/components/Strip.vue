<template>
  <div class="container" ref="container" :style="containerStyle">
    <div class="rectangle"></div>
    <div class="triangle" :style="allStyle"></div>
  </div>
</template>

<script>
  export default {
    name: "Strip",
    props: {
      height: {
        type: Number,
        default: 20
      },
      width: {
        type: Number,
        default: 60
      },
      color: {
        type: String,
        default: 'red'
      },
      direction: {
        type: String,
        default: 'right'
      },
      big: {
        type: String,
        default: 'bottom'
      }
    },
    data() {
      return {
        triangleStyle: '',
        containerStyle: '',
        bigStyle: ''
      }
    },
    computed: {
      allStyle() {
        return this.bigStyle + ';' + this.triangleStyle
      }
    },
    mounted() {
      this.setData()
      // console.log(this.allStyle);
    },
    methods: {
      getRealDirection() {
        if(this.direction == 'right'){
          this.triangleStyle = 'border-left:' + this.color + ' solid ' + this.height / 2 + 'px'
          this.containerStyle = 'flex-direction: row;'
        } else{
          this.triangleStyle = 'border-right:' + this.color  + ' solid '+ this.height / 2 + 'px'
          this.containerStyle = 'flex-direction: row-reverse;'
        }
      },
      getRealBig() {
        if(this.big == 'bottom')
          this.bigStyle = 'border-bottom:' + this.height / 2 + 'px solid ' + this.color
      else
          this.bigStyle = 'border-top:' + this.height / 2 + 'px solid ' + this.color
        // console.log(this.bigStyle);
      },
      setData() {
        this.$refs.container.style.setProperty('--height',this.height + 'px')
        this.$refs.container.style.setProperty('--width',this.width + 'px')
        this.$refs.container.style.setProperty('--color',this.color)
        this.getRealDirection();
        this.getRealBig()
      }
    }
  }
</script>

<style scoped lang="scss">
  .container {
    display: flex;


    .rectangle {
      background-color: var(--color);
      height: var(--height);
      width: var(--width);
    }

    .triangle {
      height: 0px;
      width: 0px;
      border:calc(var(--height) / 2) solid transparent;
      /*border-left:calc(var(--height) / 2) solid var(--color);*/
      /*border-bottom:calc(var(--height) / 2) solid var(--color);*/
    }
  }
</style>