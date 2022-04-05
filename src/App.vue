<template>
  <div id="app" class="container">
    <Header>
      <h1>Vizsga</h1>
      <nav>
        <ul class="nav">
          <li class="nav-item">
            <a class="nav-link" href="#">Táblázat</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Form</a>
          </li>
        </ul>
      </nav>
    </Header>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <VizsgaItem />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VizsgaItem from './components/VizsgaItem.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    VizsgaItem
  }
}
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
