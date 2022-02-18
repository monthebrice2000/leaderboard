<template>
  <div class="item params">
    <div class="param" @click="search(7)">7 Days</div>
    <div class="param" @click="search(30)">30 Days</div>
    <div class="param active" @click="search(31)">All Times</div>
  </div>
</template>

<script>
  import $ from 'jquery';
  $(".param").click(function () {
    console.log("Click");
    $("param").removeClass("active");
    $(this).addClass("active");
  });

  export default {
    name: 'Params',
    emits: [ 'search' ],
    methods : {
      search( day ){
        this.$emit( 'search', day );
      }
    },
    mounted() {
      $(".param").click(function () {
        console.log("Click");
        $(".param").removeClass("active");
        $(this).addClass("active");
      });
    }

  }


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
