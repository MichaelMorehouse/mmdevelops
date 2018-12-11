<template>
    <header>
        <img class="splash-image" src='../../assets/profile.png'>
        <h1 class="text-uppercase text-centered">Michael M Miller</h1>
        <h2>Software Developer - Data Analyst</h2>
    </header>
</template>

<script>
export default {
    name: 'page-header'
}
</script>

<style>
    header {
        background-color: rgba(45, 100, 45, 0.9);
        color: white;
        align-content: center;
        text-align: center;
    }

    .splash-image {
        display: block;
        margin: auto;
        padding-top: 30px;
    }
</style>
