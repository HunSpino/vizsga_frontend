<template>
  <div id="app" class="container">
    <header>
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
    </header>
    <main class="row">
      <VizsgaItem :vizsga="vizsga"/>
    </main>
  </div>
</template>

<script>
import VizsgaItem from './components/VizsgaItem.vue'

export default {
  name: 'App',
  components: {
    VizsgaItem
  },
  data(){
        return{
            vizsga:{
                id: null,
                targy: '',
                tipus: '',
                kezdes: ''
            },
          
        }
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
