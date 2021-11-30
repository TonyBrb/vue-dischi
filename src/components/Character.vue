<template>
  <div class="col-2 text-center mt-5">
    <img :src="character.poster" alt="character.title">
    <h5>{{character.title}}</h5>
    <h6>{{character.author}}</h6>
    <h6 class="last">{{character.year}}</h6>
  </div>
</template>

<script>
export default {
  name: 'Character',
  props:{
    character: Object
  }
}
</script>

<style lang="scss" scoped>
  div{
    margin-right: 30px;
    background-color: #2E3A46;
    color: white;
    img{
      width: 100%;
      margin-top: 10px;
    }
    h5{
      text-transform: uppercase;
      font-size: 16px;
      font-weight: bold;
      margin-top: 10px;
      margin-bottom: 30px;
    }

    h6{
      color: #5B666E;
      margin-bottom: 0;
    }

    .last{
      margin-bottom: 60px;
    }
  }
</style>