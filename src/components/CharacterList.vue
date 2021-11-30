<template>
  <div class="row pb-5">

    <Character 
    v-for="(character,index) in filteredCharacters"
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
  props:{
    genreToSearch: String
  },
  data(){
    return{
      characters:[],
      typeToSearch:''
    }
  },
  computed:{
    filteredCharacters(){
      if(this.genreToSearch===''){
        return this.characters;
      }
      return this.characters.filter(characters => characters.genre === this.genreToSearch);
    }
  },
  methods:{
    getApi(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( r => {
        this.characters = r.data.response;
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