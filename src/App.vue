<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layout/Header';

export default {
  name:"app",
  components: {
    Header
  }
}
</script>


<style lang="scss">

   $color-grey : #555;
   $color-white : #fff;
   $color-grey-dark : #666;

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

 
  
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

  .btn {
    display: inline-block;
    border: none;
    background: $color-grey;
    color: $color-white;
    padding: 7px 20px;
    cursor: pointer;
  }

  .btn:hover {
    background: $color-grey-dark;
  }
</style>
