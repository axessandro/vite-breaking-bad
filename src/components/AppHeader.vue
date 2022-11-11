<script>
import {store} from "../store";

export default{
    name: "AppHeader",
    data(){
        return{
            filterOptions: ["Breaking Bad", "Better Call Saul"],
            store
        }
    }
}
</script>

<template>
    <header>
        <div class="container d-flex flex-column align-items-center">
            <div class="titling">
                <img src="/logo.png" alt="">
                <h1>Breaking Bad API</h1>
            </div>
            <select name="select" @change="$emit('filterApplied')" id="select" v-model="store.filterOption">
                <option selected value="select">Select category</option>
                <option v-for="(option, index) in filterOptions" :key="index" :value="option">{{option}}</option>
            </select>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/styles/general.scss" as *;
.titling{
    display: flex;
    align-items: center;
    background-color: $secondary-color;
    border-radius: 70px;
    padding: 0 2rem;
    margin: 20px 0;
    img{
        height: 50px;
    }
    h1{
        padding: 2rem;
    }
}


select{
    padding: 1rem 2rem;
    border-radius: 30px;
}


</style>