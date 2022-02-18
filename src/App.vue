<template>
  <Title />
  <Params @search="search"/>
  <Leaders :day="day"/>
</template>

<script>
import Title from "./components/Title.vue";
import Params from "@/components/Params";
import Leaders from "@/components/Leaders";

export default {
  name: "App",
  components: {
    Title,
    Params,
    Leaders,
  },
  data : function(){
    return {
      day : 31,
    }
  },
  methods : {
    search( day_ ){
      this.day = day_;
      console.log(day_ , typeof day_ )
    }
  }
};


</script>

<style></style>
