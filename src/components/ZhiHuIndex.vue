<template>
  <component :toggleComponent="toggleComponent" :is="typeName"></component>
</template>

<script>
export default {
  name: 'ZhiHuIndex',
  data () {
    return {
      typeName: 'Login'
    }
  },
  methods:{
    toggleComponent:function(){
      this.typeName=this.typeName==="Login"?"Register":"Login"
    }
  },
  components:{
    Login,
    Register
  }
}
import Login from "./Login"
import Register from "./Register"
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
