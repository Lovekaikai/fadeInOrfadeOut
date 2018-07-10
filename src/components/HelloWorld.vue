<template>
  <div class="hello">
    <button @click="btn">按钮</button>
      <transition   name="bounce"
    enter-active-class="animated fadeInRight"
  leave-active-class=" animated fadeOutRight">
         <index v-if="show"></index>
      </transition>
  </div>
</template>

<script>
import index from './index'
export default {
  name: 'HelloWorld',
  data () {
    return {
      show:false,
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    index
  },
  methods:{
    btn(){
      this.show=!this.show
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import  'animate.css';

.hello{
  width:100vw;
  height:100vh;
  background:red;
  position:relative; 
}
.right{
  top:0;
  right:0;
  position:absolute;
}
</style>
