<template>
    <footer>
        <div>Built with care and <a href="https://vuejs.org/" target="_blank">Vue.js</a></div>
        <div>Copyright &copy; Michael M Miller 2018</div>
    </footer>
</template>

<script>
export default {
    name: 'page-footer'
}
</script>

<style>
    footer {
        text-align: right;
        font-size: .7em;
        background-color: rgb(44, 62, 80);
        color: white;
        padding: 10px;
    }

    footer>div:not(:last-child) {
        padding-bottom: 5px;
    }

    footer a {
        color: white;
    }

</style>