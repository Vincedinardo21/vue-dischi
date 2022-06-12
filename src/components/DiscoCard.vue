<template>
    <div class="card">
        <img :src="discoObject.poster" :alt="discoObject.title">
        <h2>{{discoObject.title}}</h2>
        <div>{{discoObject.author}}</div>
        <div>{{discoObject.year}}</div>
    </div>
</template>

<script>
export default {
  name: 'DiscoCard',
  props: {
      discoObject : Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
 .card {
    flex-basis: calc(100% / 6);
    border: 1px solid black;
    background-color: aquamarine;
    min-height: 400px;
    padding: 20px;
    margin: 10px;

    img {
        width: 100%;
    }

    h2 {
        color: white;
        margin: 20px 0;
    }
 }
</style>