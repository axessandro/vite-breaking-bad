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
      store,
    }
  },
  
  methods:{
    filterCharacters(){
      if(this.store.filterOption){
        const param = this.store.filterOption;
        let apiUrl = `https://www.breakingbadapi.com/api/characters?category=${param}`;
        console.log(apiUrl);
        axios.get(apiUrl).then((resp) =>{
          this.store.allCharacters = resp.data;
        })
      }
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
  <AppHeader @filterApplied="filterCharacters"/>
  <AppMain/>
</template>

<style lang="scss">
@use "./assets/styles/general.scss" as *;

</style>
