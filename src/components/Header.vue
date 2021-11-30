<template>
  <div>
    <img src="../../public/spotify-logo.png" alt="">
    <select class="form-select" v-model="type" @change="$emit('changeGenre',type)">
      <option value="" selected>Search for genre</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
  </select>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      type: ''
    }
  },
  methods:{
  },
  mounted(){
  }

}
</script>

<style lanf="scss" scoped>
  div{
    height: 50px;
    background-color: #2E3A46;
  }
  img{
      margin-left: 20px;
      width: 50px;
      height: 100%;
    }
  .form-select{
    width: 200px;
    float: right;
    margin-top: 5px;
    margin-right: 10px;
  }

</style>