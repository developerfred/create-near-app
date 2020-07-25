<template>
  <div id="app">
    <img alt="Near Blockchain logo" src="../assets/logo.png">
    <HelloNear msg="Welcome to NEAR!"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import HelloNear from './HelloNear.vue'
import NotSigned from './NotSigned.vue'

import 'regenerator-runtime/runtime'
import { login, logout, onSubmit } from './utils'
import '../global.css'

import getConfig from '../config'

const { networkId } = getConfig(process.env.NODE_ENV || 'development')

@Component({
  components: {
    HelloNear
  }
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
