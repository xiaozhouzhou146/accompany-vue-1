<template>
  <div id="app">
    <navigtion></navigtion>
    <index></index>
  </div>
</template>

<script>
import navigtion from './components/navigtion';
import index from './components/index/index'
export default {
  name: "App",
  components: { navigtion,index },
};

</script>

<style>
</style>
