<template>
    <div>
        {{ name }} - {{ description }}
    </div>
</template>

<script>

export default {
    name: 'skill-item',
    props: {
        name: String,
        description: String,
    }
}
</script>

<style>
</style>