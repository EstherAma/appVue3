<script>
import ChildComponent from './ChildComponent.vue'
export default {
  components: { ChildComponent },
    data() {
        return {
            movieTitle:'Batman',
            brandParent : "",
            count : 0,
        }
    },
    methods: {
        receivedBrand(data) {
            this.brandParent= data;
            this.count++;
        }
    },

}
</script>

<template>
    <h2>I am your father</h2>
    <span>{{ movieTitle }}</span>
    <Child-component :movieTitle="movieTitle" @brand="receivedBrand"/>
    <span>   BRAND : {{ brandParent }} / {{ count }}</span>
    <div>
        
    </div>
</template>

<style lang="css" scoped>
h2 {
    color: green;
}
</style>