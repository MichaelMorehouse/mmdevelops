<template>
    <div id="navbar-container" class="navbar-top">
        <div class="navbar-flex text-uppercase">
            <div class="navitem home-item"><a href='#'>MMM</a></div>
            <div class="navitem"><a href='#about-me'>About Me</a></div>
            <div class="navitem"><a href='#skills'>Skills and Projects</a></div>
            <div class="navitem navitem-right"><a href='#contact'>Connect</a></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'navigation-bar',
    data: function() {
        return {
        }
    }
}
</script>

<style scoped>

    #navbar-container {
        display: inline;
    }

    .navbar-top {
        position: sticky;
        top: 0;
    }

    .navbar-flex {
        display: flex;
        background-color: rgb(44, 62, 80);
        align-items: baseline;
    }

    .navitem {
        float: left;
        margin: 0;
        padding: 0;
        overflow: hidden;
        box-shadow: 0px 4px 2px -2px rgb(100, 100, 100, .4);
    }

    .navitem-right {
        margin-left: auto;
        margin-right: 10px;
    }

    .home-item {
        font-size: 1.2em;
        margin-left: 10px;
    }

    .navitem a {
        display: block;
        margin: 15px 5px;
        padding: 10px 14px;
        color: white;
        text-align: center;
        text-decoration: none;
        border-radius: 2px;
        transition: 0.15s background-color linear;
    }

    a:hover {
        background-color: rgb(40, 95, 145, 0.5);
    }

</style>
