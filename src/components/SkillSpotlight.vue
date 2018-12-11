<template>
    <div id="skill-spotlight">
        {{ skill.name }}
        <div v-for="(bullet, index) in skill.bullets" :key="index">
            {{ bullet }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'skill-spotlight',
    data: function() {
        return {
            skill: {
                name: String,
                bullets: Array
            }
        }
    }
}
</script>

<style>

</style>
