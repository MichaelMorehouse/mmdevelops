<template>
    <div class="project-item" v-on:click="$emit('activate-project')" :class="isActive ? 'active-project' : ''">
        <div class="project-title">{{ project.name }}</div>
        <div v-if="project.icon">
            <img class="project-icon" :src="require('@/assets/' + project.icon)" alt="I'm missing!" >
        </div>
    </div>
</template>

<script>
export default {
    name: 'project-item',
    data: function() {
        return {
        }
    },
    props: {
        project: {
            name: String,
            bullets: Array,
        },
        isActive: Boolean
    },
}
</script>

<style>
    .project-item {
        padding: 10px 10px;
        border: 1px solid  rgb(44, 62, 80, .4);
        border-radius: 2px 2px 10px 2px;
        -webkit-box-shadow: 1px 1px 0px 0px rgba(44, 62, 80, 0.4);
        -moz-box-shadow:    1px 1px 0px 0px rgba(44, 62, 80, 0.4);
        box-shadow:         1px 1px 0px 0px rgba(44, 62, 80, 0.4);
    }

    .project-item:hover {
        border-color: rgb(44, 62, 80, .6); 
        cursor: pointer;
        -webkit-box-shadow: 1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        -moz-box-shadow:    1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        box-shadow:         1px 2px 1px 0px rgba(44, 62, 80, 0.6);
    }

    .project-item:not(.active-project):hover {
        border-color: rgb(44, 62, 80);
    }

    /* Project title styles */
    .project-title {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 0 5px 0;
        border-bottom: 1px solid  rgb(44, 62, 80);
        min-height: 2.5em;
    }

    /* Project icon styles */

    .project-icon {
        max-width: 70%;
        padding: 20px 10px;
        opacity: .5;
    }

    .project-item:not(.active-project):hover .project-icon {
        opacity: .8;
    }

    .active-project .project-icon {
        opacity: 1;
    }
</style>