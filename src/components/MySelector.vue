<template>
    
        
    <option :value="genreObject.genre">{{genreObject.genre}}</option>
            <!-- <option value="rock" @click="$emit('myGenre', inputGenre)">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option> -->
        
    
</template>

<script>

export default {
    name: 'MySelector',
    props: {
        genreObject : Object
    },
    data(){
        return {
           inputGenre: "",
        }
    },
  
    methods: {
        
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   
</style>