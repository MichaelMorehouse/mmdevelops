<template>
    <div id="contact-container">
        <h2 class="text-uppercase">Connect with Me</h2>
        <div>
            <a v-bind:href="'mailto:' + email.address + '?subject=' + email.defaultSubject">Email</a>
            <a v-bind:href="linkedin">LinkedIn</a>
            <a v-bind:href="github">Github</a>
        </div>
    </div>
</template>

<script>
export default {
    name:"contact-container",
    data: function() {
        return {
            email: { address: 'mmdevelops@gmail.com', defaultSubject: 'Hello Michael!' },
            linkedin: 'https://www.linkedin.com/in/mmorehousemiller',
            github: 'https://github.com/MichaelMorehouse'
        }
    }
}
</script>

<style>
    #contact-container {
        color: white;
        background-color: rgb(44, 62, 80, .9);
        text-align: center;
        padding: 20px 10px;
    }
</style>
