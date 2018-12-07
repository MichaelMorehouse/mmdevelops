<template>
    <div id="navbar-container" class="navbar-top">
        <div class="home-item"><a href='/'>MMM</a></div>
        <div><a href='#skills'>Skills and Projects</a></div>
        <div class="navitem-right"><a href='#contact'>Contact Me</a></div>
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

    .navbar-top {
        position: sticky;
        top: 0;
    }

    #navbar-container {
        display: flex;
        background-color: rgb(44, 62, 80);
        align-items: baseline;
    }

    #navbar-container > div{
        float: left;
        margin: 0;
        padding: 0;
        overflow: hidden;
        box-shadow: 0px 4px 2px -2px rgb(100, 100, 100, .4);
    }

    #navbar-container > div.navitem-right {
        margin-left: auto;
    }

    #navbar-container > div.home-item {
        font-size: 1.2em;
    }

    a {
        margin: 8px 4px;
        display: block;
        color: white;
        text-align: center;
        padding: 10px 14px;
        text-decoration: none;
        border-radius: 2px;
        transition: 0.15s background-color linear;
    }

    a:hover {
        background-color: rgb(40, 95, 145, 0.5);
    }

</style>
