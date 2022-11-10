<script>
export default{
    name: "AppHeader",
}
</script>

<template>
    <header>
        <div class="container d-flex flex-column align-items-center">
            <h1>Breaking Bad API</h1>
            <select name="select" id="select">
                <option value="select">Select category</option>
                <option value="select">Alive</option>
                <option value="select">Dead</option>
            </select>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/styles/general.scss" as *;

h1{
    padding: 2rem;
}

select{
    padding: 1rem 2rem;
    border-radius: 30px;
}


</style>