<template>
  <div>
    <div class="main-wrapper">
      <Header />
      <div class="container">
        <CharacterList />
      </div>
      
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import CharacterList from './components/CharacterList.vue'


export default {
  name: 'App',
  components: {
    Header,
    CharacterList
    
  }
}
</script>

<style lang="scss">

@import "./assets/style/general.scss";

.main-wrapper{
  min-height: 100vh;
  background-color: #1E2D3B;
}
</style>
