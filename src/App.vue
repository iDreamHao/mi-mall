<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
 data() {
   return {
     
   }
 },
 mounted(){
   this.getData();
 },
 methods:{
   getData:function(){
     this.axios.get('/user/login')
     .then((res)=>{
       console.log('res :>> ', JSON.stringify(res));
     })
     .catch(()=>{

     })
   }
 }
};
</script>

<style>

</style>
