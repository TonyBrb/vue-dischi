<template>
  <div class="row">

    <Character 
    v-for="(character,index) in characters"
    :key="index"
    :character="character"
    />

  
  </div>
</template>

<script>

import axios from "axios";
import Character from "./Character";

export default {
  name: 'CharacterList',
  components:{
    Character,
  },
  data(){
    return{
      chatacters:[]
    }
  },
  methods:{
    getApi(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( r => {
        this.chatacters = r.data;
      })
      .catch( e => {
        console.log(e);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}

</script>

<style lang="scss">

</style>