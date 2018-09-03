<template>
  <div id="app">
    <ZhiHuIndex/>
  </div>
</template>

<script>
import ZhiHuIndex from './components/ZhiHuIndex'

export default {
  name: 'App',
  components: {
    ZhiHuIndex
  }
}
</script>

<style>
body { 
  background-image: url("./assets/sign_bg.png");
  width:100vh;
  height: 100%;
}
</style>
