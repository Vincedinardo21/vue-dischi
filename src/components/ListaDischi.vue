<template>
    <section>
        <div class="card-container">
            <DiscoCard v-for="(item, i) in dischi" :key="i" :discoObject="item"/>
        </div>      
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
            this.dischi = result.data.response;
            console.log(result);
            })
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    section {
        padding: 30px;
        background-color: rgb(30, 45, 59);

        .card-container {
            width: 80%;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
    }
</style>