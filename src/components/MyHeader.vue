<template>
    <header>
        <!-- <h1>My Header</h1> -->
        <img src="../assets/logo-spotify-icon-1536.png" alt="">
    </header>
</template>

<script>
export default {
  name: 'MyHeader',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header {
    padding: 5.5px;
    display: flex;
    background-color: rgb(46, 58, 70);

    img {
      width: 50px;
    }
  }
</style>
