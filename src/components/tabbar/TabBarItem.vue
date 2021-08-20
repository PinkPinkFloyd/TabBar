<template>
  <div class="tab-bar-item" @click="itemClick">
     <div v-if="!isActive"><slot name="item-icon"></slot></div>
     <div v-else><slot name="item-icon-active"></slot></div>
     
     <div :style="activeStyle"><slot name="item-text"></slot></div>
     
     
     
  </div>
</template>

<script>
export default {
name:"TabBarItem",
data(){
  return {
    
  }
},
computed:{
isActive(){
  return !this.$route.path.indexOf(this.path) 
},
activeStyle(){
  return this.isActive ? {color:this.activeColor} : {}
}
},
props:{
path:String,
activeColor:{
  type:String,
  default:'red'
}
},
methods:{
  itemClick(){
    this.$router.replace(this.path).catch(err=>err)
  }
}
}
</script>

<style>
/* 父元素开启flex布局，子元素flex:1可以均等分父元素
text-align:center 居中
*/
.tab-bar-item{
  flex: 1;
  text-align: center;
  height: 49px;      
}
.tab-bar-item img{
  width: 24px;
  height: 24px;

}
.active{
  color: red;
}
</style>