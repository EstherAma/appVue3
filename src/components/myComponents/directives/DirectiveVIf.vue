<script setup></script>

<script>
export default {
    data(){
        return{
            movies: [],
            newTitle: '',
            adding: false,
        }
    },
    methods: {
        addMovie(){
            this.movies.push({
                id: this.movies.length + 1,
                title: this.newTitle,
            })
            this.newTitle = ''
        },
        showInputToAdd(state){
            this.adding = state
            this.newTitle = ''
        },
    },
}
</script>

<template>
    <div>
        <h2>---- Directives v-if and v-else ----</h2>
        <label class="m-3">Testing directive v-if and v-else     </label>
        <button class="btnAddMovie"
            v-if="adding == false"
            v-on:click="showInputToAdd(true)">
            Add Movie
        </button>
        <button class="btnCancel"
            v-else
            v-on:click="showInputToAdd(false)">
            cancel
        </button>
        <div v-if="adding">
            <input 
                id="add-movie-input"
                @keyup.enter="addMovie()"
                v-model="newTitle"
                placeholder="Add a movie"
            />
            <button v-on:click="addMovie()" class="btnPlus btn btn-primary">+</button>
        </div>
        <span v-if="movies.length == 0" class="m-3">    Please add movie</span>
        <ul class="m-3">
            <template v-for="(movie, key) in movies" :key="movie.id">
                <li :id="key">{{ movie.id }}: {{ movie.title }}</li>
            </template>
        </ul>
    </div>
</template>

<style lang="css" scoped>
h2{
    color: orange
}
.btnAddMovie{
    width: 90px;
    height: 35px;
    background-color: steelblue;
    border: none;
    color: white;
    border-radius: 5px;
    box-shadow: 3px 3px 10px rgba(0,0,0, .75);
}

.btnAddMovie:hover{
    background:rgb(227, 103, 58);
}

.btnCancel{
    width: 55px;
    height: 20px;
    background-color: none;
    border: 2px solid crimson;
    color: crimson;
    border-radius: 5px;
    box-shadow: 3px 3px 10px rgba(0,0,0, .50);
}

.btnCancel:hover{
    background:rgb(227, 103, 58);
    color: antiquewhite;
}

.btnPlus{
    width: 26px;
    height: 21px;
    background-color: none;
    border: 2px solid green;
    color: green;
    border-radius: 3px;
    box-shadow: 2px 2px 8px rgba(44, 44, 44, 0.5);
}

.btnPlus:hover{
    background:green;
    color: antiquewhite;
}
span{
    color: steelblue;
    font-weight: bold;
}

</style>