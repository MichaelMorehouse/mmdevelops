<template>
    <header>
        <img class="splash-image" src='../../assets/profile.png'>
        <h1 class="text-uppercase text-centered">Michael M Miller</h1>
        <h2> Software Developer - Data Analyst </h2>
    </header>
</template>

<script>
export default {
    name: 'page-header'
}
</script>

<style>
    header {
        background-color: rgb(39, 197, 39, 0.8);
        align-items: center;
    }

    .splash-image {
        display: block;
        margin: auto;
        padding: 10px;
    }
</style>
