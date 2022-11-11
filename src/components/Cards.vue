<script>
import {store} from "../store";

export default{
    name: "Cards",
    data(){
        return{
            store
        }
    },
    props:{
        name: String,
        status: String,
        url: String,
        series: String,
    }
}
</script>

<template>
<div class="ms-card">
    <div class="img-wrapper">
        <img :src="url" alt="">
    </div>
    <div class="identity">
        <h2>{{name}}</h2>
        <h6>{{series}}</h6>
        <p>{{status}}</p>

    </div>
</div>
</template>

<style lang="scss" scoped>
@use "../assets/styles/general.scss" as *;

.ms-card{
    background-color: $primary-color;
    padding: .7rem;
    min-height: 500px;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    .img-wrapper{
        width: 100%;
        img{
            width: 100%;
            border-radius: 20px;
        }
    }
    .identity{
        padding-top: .7rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        h2{
            font-size: 1.2rem;
            padding-bottom: 1rem;
            text-align: center;
        }
        h6{
            font-weight: 200;
            font-size: 1.5rem;
            opacity: .4;
            text-align: center;
        }
        p{
            font-weight: 200;
            opacity: .4;
            text-align: center;
        }
    }
}

</style>