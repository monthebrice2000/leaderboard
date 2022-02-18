<template>
  <div class="item leaders">
    <Leader v-for="leader in users_" :key="leader" :name="leader.name" :score="leader.score" :image="leader.src" :country="leader.country"/>
    <div v-if="!this.day || this.day===null" class="leader"> No Users</div>
  </div>
</template>

<script>
  import Leader from "@/components/Leader";
export default {
  name: 'Leaders',
  props : [ 'day' ],
  components : {
    Leader
  },
  data: function(){
    return {
      day_ : this.day,
      users : [
        { score : 2000, name : 'MONTHE BRICE', country : 'FRANCE', src : './img/network.jpg', day : 5},
        { score : 2000, name : 'MONTHE BRICE', country : 'FRANCE', src : './img/network.jpg', day : 12},
        { score : 2000, name : 'MONTHE BRICE', country : 'FRANCE', src : './img/network.jpg', day : 25},
        { score : 2000, name : 'MONTHE BRICE', country : 'FRANCE', src : './img/network.jpg', day : 50},
        { score : 2000, name : 'MONTHE BRICE', country : 'FRANCE', src : './img/network.jpg', day : 70},
        { score : 2000, name : 'MONTHE BRICE', country : 'FRANCE', src : './img/network.jpg', day : 100}
      ]
    }
  },
  watch : {
    day_( newVal, oldVal ){
      console.log( newVal, oldVal )
    }
  },
  computed : {
    users_ (){
      if( this.day >= 31 ){
        return this.users;
      }
      return this.users.filter( leader => leader.day <= this.day );
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
