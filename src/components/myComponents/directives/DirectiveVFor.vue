<script>
export default {
    data() {
        return {
            list: ['spain', 'frances', 'italy'],
        }
    },
}
</script>

<template>
    <div>
        <h2>--- v-for directive ---</h2>
        <ul>
            <template v-for="(country, key) in list" :key="key">
                <li :id="[key + 1]"> {{ key }}: {{ country }}</li>
                    
            </template>
        </ul>
    </div>
</template>

<style lang="css" scoped>
h2{
    color: orange
}
</style>