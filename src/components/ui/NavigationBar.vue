<template>
    <div id="navbar-container" class="navbar-top">
        <div class="navbar-flex text-uppercase">
            <div id="nav-home" class="nav-item" v-on:click="scrollToTop">MMM</div>
            <div id="nav-connect" v-on:click="scrollToTarget" targetId="connect" class="nav-item nav-item-right">Connect</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'navigation-bar',
    data: function() {
        return {
        }
    },
    methods: {
        scrollToTop: function() {
            window.scrollTo({
                top: 0,
                left: 0
            })
        },
        scrollToTarget: function(event) {
            document.getElementById(event.srcElement.attributes.targetId.value).scrollIntoView();
        }
    }
}
</script>

<style>

    #navbar-container {
        display: block;
        z-index: 1;
    }

    #nav-home {
        font-size: 1.2em;
        margin-left: 10px;
    }

    .navbar-top {
        position: sticky;
        top: 0;
    }

@media screen and (max-width: 600px) {
    .navbar-top {
        position: relative;
    }
}

    .navbar-flex {
        display: flex;
        background-color: rgb(44, 62, 80);
        align-items: baseline;
    }

    /* Navigation item styles */
    .nav-item {
        display: block;
        float: left;
        overflow: hidden;
        margin: 10px 5px;
        padding: 10px 14px;
        color: white;
        text-align: center;
        text-decoration: none;
        border-radius: 2px;
        transition: 0.15s background-color linear;
    }

    .nav-item-right {
        margin-left: auto;
        margin-right: 10px;
    }

    .nav-item:hover {
        cursor: pointer;
        background-color: rgb(40, 95, 145, 0.5);
    }

</style>
