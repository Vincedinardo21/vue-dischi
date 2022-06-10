<template>
    <div class="card">
        <!-- <img :src="discoObject.poster" :alt="discoObject.title"> -->
        <!-- <h2>{{discoObject.title}}</h2> -->
        <div>{{discoObject.author}}</div>
        <div>Anno</div>
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

</style>