<template>
  <DollarExchange />
</template>

<script>
import DollarExchange from '@/components/DollarExchange';

export default {
  name: 'App',
  components: {
    DollarExchange
  }
}
</script>

<style>
body{
  background-color: #001835;
  width: 300px;
  height: 200px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
