<script>
export default {
    props: {
        movieTitle: String,
    },
    data() {
        return {
            brandChild: 'DC Comics',
        }
    },
    methods: {
        sendBrand() {
            this.$emit('brand', this.brandChild)
        }
    }
}
</script>

<template>
    <h2>Hijita {{ movieTitle }}ita</h2>
    <button @click="sendBrand">SendBrand</button>
</template>

<style lang="css" scoped>
h2 {
    color: green;
}
button {
    width: 90px;
    height: 35px;
    background-color: green;
    border: none;
    color: white;
    border-radius: 5px;
    box-shadow: 3px 3px 10px rgba(0,0,0, .50);
}

</style>