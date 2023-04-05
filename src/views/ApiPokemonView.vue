<script>
import ApiChuckNorris from '../components/myComponents/apiComponent/ApiChuckNorris.vue'
import ApiPokemon from '../components/myComponents/apiComponent/ApiPokemon.vue'


export default {
  components: { ApiPokemon, ApiChuckNorris },
}
</script>

<template>
    <api-pokemon />
    -----------------------------------------
    <h1>Chuck Norris Api</h1>
    <api-chuck-norris />
</template>

<style>

</style>


