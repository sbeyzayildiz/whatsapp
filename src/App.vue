<template>
<div id="App">
  <div class="container app">
    <div class="app-one">
      <center></center>
    </div>    
  </div>
</div>
</template>

<script>
import Center from './components/Center'
export default {
  name: 'App',
  components: {Center},
  
}

</script>

<style scoped>
@media screen and (max-width: 700px)
{
html,
body,
div,
span {
  height: 100%;
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background: url("http://shurl.esy.es/y") no-repeat fixed center;
  background-size: cover;
}

.fa-2x {
  font-size: 1.5em !important;
}

.app {
  position: relative;
  overflow: hidden;
  top: 19px;
  height: calc(100% - 38px);
  margin: auto !important;
  padding: 0 !important;
  box-shadow: 0 1px 1px 0 rgba(0, 0, 0, .06), 0 2px 5px 0 rgba(0, 0, 0, .2);
}
.app-one {
  background-color: #f7f7f7;
  height: 100%;
  overflow: hidden;
  margin: 0 !important;
  padding: 0 !important;
  box-shadow: 0 1px 1px 0 rgba(0, 0, 0, .06), 0 2px 5px 0 rgba(0, 0, 0, .2);
}
}


</style>
