<template>
  <nuxt-link title="Click to view Profile" :to="'/users/'+ id">
    <div class="f-left">
       <div class="img" :style="{backgroundImage:'url('+ image +')'}"></div> 
      <div class="txt">{{ name }}</div>
      <div class="txt-mail">{{ email }}</div>
     </div>
  </nuxt-link>
</template>
<script>
 export default{
  props:['image','name','id','email']
 }; 
</script>
<style scoped>
a{
  color: black;
}
  .f-left{
      float: left;
      width: 300px;
      background: white;
      margin-left: 5%;
      border: 1px solid #95afc0;
      height: 250px;
      margin-top: 1%;
      box-shadow: 0 2px 2px #aaa;
}
.f-left .img{
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}
.f-left .txt{
    text-align: center;
}
.f-left .txt-mail{
    text-align: center;
    color: #2980b9;
}
</style>