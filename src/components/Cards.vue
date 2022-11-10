<script>
import {store} from "../store";

export default{
    name: "Cards",
    data(){
        store
    },
}
</script>

<template>
<div class="ms-card">
    <p></p>
    <p>Name</p>
    <p>Breaking Bad</p>
    <p>Alive?</p>
</div>
</template>

<style lang="scss" scoped>
@use "../assets/styles/general.scss" as *;


</style>