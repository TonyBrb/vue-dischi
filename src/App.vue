<template>
  <div>
    <div class="main-wrapper">
      <Header />

    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'


export default {
  name: 'App',
  components: {
    Header
    
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
