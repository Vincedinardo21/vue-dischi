<template>
    <section>
        <!-- <h2>ListaDischi</h2> -->
        <DiscoCard
            v-for="(item, i) in dischi" :key="i" :discoObject = "item"

        />
    </section>
</template>

<script>
import axios from "axios"
import DiscoCard from "./DiscoCard.vue";

export default {
    name: 'ListaDischi',

    //componenti del figlio 
    components : {
    DiscoCard
},
  data(){
      return {
          apiUrl : "https://flynn.boolean.careers/exercises/api/array/music",
          dischi : []
      }
  },
  created(){
      this.getDisco();
  },
    methods: {
        getDisco(){
        axios.get(this.apiUrl)
        .then((result) => {
            this.dischi = result.data;
            console.log(result);
            })
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>