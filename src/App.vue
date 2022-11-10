<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import {store} from "./store";

export default{
  components:{
    AppHeader,
    AppMain
  },

  data(){
    return{
      store
    }
  },

  created(){
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp)=>{
      this.store.allCharacters = resp.data;
    });
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
</template>

<style lang="scss">
@use "./assets/styles/general.scss" as *;

</style>
