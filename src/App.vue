<template>
  <div id="app">
    <info/>
    <Form
      v-for="form in forms"
      v-bind:form="form"
    />
  </div>
</template>

<script>
import Form from './components/Form.vue'
import Info from './components/Info.vue'

export default {
  name: 'App',
  data() {
    return{
      forms:[
        {top: '90', title: 'Step 3', color: '#d85959', left: '80'},
        {top: '130', title: 'Step 2', color: '#5990d8', left: '40'},
        {top: '170', title: 'Step 1', color: '#38864c', left: '0'}
      ]
    }
  },
  components: {
    Form,
    Info
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fefffb;
  width: 100%;
  height: fit-content;
  margin: 0;
  padding: 0;
}
</style>
