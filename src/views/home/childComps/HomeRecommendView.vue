<template>
  <div class="recommend">
    <div v-for="item in recommends" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>

</template>

<script>
    export default {
        name: "",
      props:{
          recommends:{
            type:Array,
            default(){

            }
          }
      }
    }
</script>

<style scoped>
  .recommend {
    display: flex;
    /*width: 100%;*/
    text-align: center;
    font-size: 12px;
    padding: 15px 0px 30px;
    border-bottom: 8px solid #eee;
  }
  .recommend-item{
    flex: 1;
  }
  .recommend-item img{
    width: 65px;
    height: 65px;
    margin-bottom: 10px;
  }
</style>
