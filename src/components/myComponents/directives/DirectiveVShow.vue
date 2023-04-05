<script setup></script>

<script>
export default {
    data(){
        return{
            isShowing : true,
        }
    },
    methods: {
        /* function changeStage() en php o js*/
        changeState(){
            if (this.isShowing) {
                this.isShowing = false;
                return
            }
            this.isShowing = true;
        }
    },
};
</script>

<template>
    <div>
        <h2>---- v-show directive ----</h2>
        <button v-on:click="changeState">
            <span v-show="isShowing">Once upon a time ...</span>

        </button>
    </div>
</template>

<style lang="css" scoped >
h2{
    color: orange
}

button{
    width: 150px;
    height: 50px;
    background-color: steelblue;
    border: none;
    color: white;
    border-radius: 5px;
    box-shadow: 3px 3px 10px rgba(0,0,0, .75);
}

button:hover{
    background:rgb(227, 103, 58);
}
</style>