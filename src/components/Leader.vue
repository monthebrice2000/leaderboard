<template>
  <div class="leader">
    <div class="content">
      <div class="logo"><img :src="image"></div>
      <div class="profil">
        <h2 class="name">{{ name }}</h2>
        <h3 class="country">{{ country }}</h3>
      </div>
    </div>
    <div class="score">{{ score }}</div>
  </div>
</template>

<script>
export default {
  name: 'Leaders',
  props : [ 'name', 'country', 'score', 'image'],
  data : () => {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
