<template>
  <div class="row pb-5">

    <Character 
    v-for="(character,index) in characters"
    :key="index"
    :character="character"
    />

  
  </div>
</template>

<script>

import axios from 'axios';
import Character from "./Character";

export default {
  name: 'CharacterList',
  components:{
    Character,
  },
  data(){
    return{
      characters:[]
    }
  },
  methods:{
    getApi(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( r => {
        this.characters = r.data.response;
        console.log('characters',this.characters);
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