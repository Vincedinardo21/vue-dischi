<template>       
    <option :value="genreObject.genre">{{genreObject.genre}}</option>  
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
        getGenre(){
            //console.log("Ciao");
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   
</style>