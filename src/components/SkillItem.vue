<template>
    <div class="skill-item">
        {{ name }} 
        <div v-for="(bullet, index) in bullets" :key="index">
            <div> {{ bullet }} </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'skill-item',
    props: {
        name: String,
        bullets: Array
    }
}
</script>

<style scoped>
    .skill-item {
        border: 1px solid black;
    }
</style>