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
      <VizsgaItem 
      v-for="vizsga in vizsgas" 
      v-bind:key="vizsga.id"
      :vizsga="vizsga"/>
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
          vizsgas: []
        }
    },
    methods: {
      async loadData () {
      let Response = await fetch('localhost/phpmyadmin/vizsga')
      let data = await Response.json()
      this.vizsgas = data
    }
  },
   mounted() {
    this.loadData()
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
