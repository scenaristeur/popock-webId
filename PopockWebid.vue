<template>
  <div>
    <p>webId: {{webId}}</p>
  </div>
</template>
<script>
import store from './store'

export default {
  store,
  props:['debug'],
  name: 'PopockWebid',
  data: function () {
    return {
      webId: null
    }
  },
  created(){
    console.log('PopockWebid created')
    this.webId = this.$store.state.login.webId
    console.log("webId:", this.webId)
  },
}
</script>
