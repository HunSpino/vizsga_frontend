<template>
    <div class="card" >
  <img src="" class="card-img-top" alt="kep">
  <div class="card-body">
    <h5 class="card-title">{{ vizsga.targy }}</h5>
    <p class="card-text">{{ vizsga.tipus }}</p>
    <p class="card-text">{{ vizsga.kezdes }}</p>
  </div>
</div>
</template>

<script>
export default {
    name: 'VizsgaItem',
    props: ["vizsga"] 
}

</script>

<style>
.card{
    width: 18rem;
}
</style>