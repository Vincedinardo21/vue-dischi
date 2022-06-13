<template>
    <section>
        <select name="Genere" id="Genere" @change="getClicked(userSelector)" v-model="userSelector">
            <MySelector v-for="(element, j) in dischi" :key="j" :genreObject="element"/>
        </select>
        
        <div class="card-container">
            <DiscoCard v-for="(item, i) in filteredDischi" :key="i" :discoObject="item"/>
        </div>      
    </section>
</template>

<script>
import axios from "axios"
import DiscoCard from "./DiscoCard.vue";
import MySelector from "./MySelector.vue";

export default {
    name: 'ListaDischi',

    //componenti del figlio 
    components : {
    DiscoCard,
    MySelector
},
  data(){
      return {
          apiUrl : "https://flynn.boolean.careers/exercises/api/array/music",
          dischi : [],
          userSelector: "",
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
        },
        getClicked(element){
            this.dischi.genre = element;
            console.log(element);
        }
    },
    computed: {
        filteredDischi(){
            //return this.dischi;
            return this.dischi.filter(item => {
                return item.genre.includes(this.userSelector);
            });
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