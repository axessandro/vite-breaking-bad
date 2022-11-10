<script>
import Cards from './Cards.vue';
import {store} from "../store";


export default{
    name: "AppMain",
    components: {
        Cards
    },
    data(){
        store
    }
}
</script>

<template>
<main>
    <div class="container">
        <div class="ms-label">
            <h4>Found 62 characters</h4>
        </div>
        <div class="row row-cols-md-5">
            <div class="col" v-for="(item, index) in store.allCharacters" :key="index">
                <Cards/>
                <h1>{{item}}</h1>
            </div>
        </div>
    </div>
</main>
</template>

<style lang="scss" scoped>
@use "../assets/styles/general.scss" as *;

.container{
    background-color: white;
    padding: 1rem;
    margin-top: 2rem;

    .ms-label{
        background-color: $secondary-color;
        padding: 1.2rem;

        h4{
            margin-bottom: 0;
            font-size: 1.3rem;
        }
    }

    .row{
        padding: 1rem;
        .col{
            .ms-card{
                background-color: $primary-color;
                padding: .7rem;
            }
        }
    }
}

</style>