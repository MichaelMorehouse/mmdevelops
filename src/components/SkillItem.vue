<template>
    <div class="skill-item" v-on:click="$emit('activate-skill')">
        <div>
            <div>
                {{ skill.name }}
                <transition name="fade" mode="out-in">
                    <span v-if="!isActive" class="toggle-skill-icon">
                        <font-awesome-icon :icon="['fas','plus']" key="plus"></font-awesome-icon>
                    </span>
                    <span v-else class="toggle-skill-icon">
                        <font-awesome-icon :icon="['fa','minus']" key="minus"></font-awesome-icon>
                    </span>
                </transition>
            </div>
            <transition name="slide-fade">
                <div v-if="isActive">
                    <div v-for="(bullet, index) in skill.bullets" :key="index">
                        <div> {{ bullet }} </div>
                    </div>
                </div>
            </transition>
        </div>
    </div>
</template>

<script>

export default {
    name: 'skill-item',
    data: function() {
        return {
            isActive: false
        }
    },
    props: {
        skill: {
            name: String,
            bullets: Array,
        }
    },
    methods: {
        toggleActive: function() {
            return this.isActive = !this.isActive
        }
    }
}
</script>

<style scoped>
    .skill-item {
        border: 1px solid black;
        border-radius: 8px 0 0 0;
    }

    .toggle-skill-icon {
        float: right;
    }

    .slide-fade-enter-active {
        transition: all .3s ease;
    }
    .slide-fade-leave-active {
        transition: all .3s cubic-bezier(1.0, 0.5, 0.8, 1.0);
    }
    .slide-fade-enter, .slide-fade-leave-to {
        transform: translateX(10px);
        opacity: 0;
    }

    .fade-enter-active, .fade-leave-active {
        transition: opacity .5s;
    }
    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
        opacity: 0;
    }
</style>