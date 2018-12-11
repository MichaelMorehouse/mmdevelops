<template>
    <div id="contact">
        <h2 class="text-uppercase">Connect with Me</h2>
        <div>
            <a v-bind:href="linkedin" target="_blank">
                <font-awesome-icon :icon="['fab', 'linkedin-in']" size="3x"></font-awesome-icon>
            </a>
            <a v-bind:href="github" target="_blank">
                <font-awesome-icon :icon="['fab', 'github']" size="3x"></font-awesome-icon>
            </a>
            <a v-bind:href="'mailto:' + email.address + '?subject=' + email.defaultSubject" target="_blank">
                <font-awesome-icon :icon="['far', 'envelope']" size="3x"></font-awesome-icon>
            </a>
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

<style scoped>
    #contact {
        color: white;
        background-color: rgb(44, 62, 80, .9);
        text-align: center;
        padding: 20px 10px;
    }

    .svg-inline--fa {
        color: white;
        padding: 20px;
    }
</style>
