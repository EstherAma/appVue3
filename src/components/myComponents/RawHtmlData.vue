<script>
export default{
    data(){
        return{
            title : "These are greyhounds",
            person : {
                id: 1,
                name : "John",
                img : "https://i.pinimg.com/236x/43/99/db/4399dbbc98f93a9070844fdc12e230ce--bffs-bestfriends.jpg"
            },
            msg: "John is one of the most handsome and affectionate greyhounds"
        }
    },
};
</script>

<template>
    <h3>{{ title }}</h3>
    <div :id="person.id">
        <h4>{{ person.name }}</h4>
        <img :src="person.img" :alt="person.name">
    </div>
    <h5 v-html="msg"></h5>
</template>

<style lang="css" scoped>
h3{
    color: magenta;
}

img{
    box-shadow: 3px 3px 3px rgba(0,0,0, 0.25);
    border-radius: 10px;
}
</style>