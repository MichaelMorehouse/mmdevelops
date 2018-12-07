<template>
    <div id="navigation-bar-top">
        <ul>
            <li><a href='/'>MMM</a></li>
            <li><a href='#skills'>Skills and Projects</a></li>
            <li><a href='#contact'>Contact Me</a></li>
        </ul>
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
    #navigation-bar-top {
        position: sticky;
        top: 0;
    }

    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
        background-color: seagreen;
        box-shadow: 0px 4px 2px -2px rgb(100, 100, 100, .4);
    }

    li {
        margin: 4px;
        float: left;
    }

    li a {
        display: block;
        color: white;
        text-align: center;
        padding: 10px 14px;
        text-decoration: none;
        transition: 0.15s background-color linear;
    }

    .active {
        background-color: rgb(40, 95, 145, .9);
        border: 2px rgb(0, 0, 50, .8) solid;
    }

    li a:hover:not(.active) {
        background-color: rgb(40, 95, 145, 0.5);
        border: 2px rgb(0, 0, 50, .8) solid;
    }

    li a:not(.active) {
        border: 2px rgb(0, 0, 50, .5) solid;
    }
</style>
