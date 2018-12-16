<template>
    <div class="skill-item" v-on:click="$emit('activate-skill')" :class="isActive ? 'active-skill' : ''">
        <div>
            <div class="skill-title">{{ skill.name }}</div>
            <div v-if="skill.icon">
                <img class="skill-icon" :src="require('@/assets/' + skill.icon)" alt="I'm missing!" >
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'skill-item',
    data: function() {
        return {
        }
    },
    props: {
        skill: {
            name: String,
            bullets: Array,
        },
        isActive: Boolean
    },
}
</script>

<style>

    .skill-item {
        padding: 10px 10px;
        border: 1px solid  rgb(44, 62, 80, .4);
        border-radius: 2px 2px 10px 2px;
        -webkit-box-shadow: 1px 1px 0px 0px rgba(44, 62, 80, 0.4);
        -moz-box-shadow:    1px 1px 0px 0px rgba(44, 62, 80, 0.4);
        box-shadow:         1px 1px 0px 0px rgba(44, 62, 80, 0.4);
    }

    .skill-item:hover {
        border-color: rgb(44, 62, 80, .6); 
        cursor: pointer;
        -webkit-box-shadow: 1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        -moz-box-shadow:    1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        box-shadow:         1px 2px 1px 0px rgba(44, 62, 80, 0.6);
    }

    .skill-item:not(.active-skill):hover {
        border-color: rgb(44, 62, 80);
    }

    /* Skill title styles */
    .skill-title {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 5px 10px;
        border-bottom: 1px solid  rgb(44, 62, 80);
        min-height: 45px;
    }

    /* Skill icon styles */

    .skill-icon {
        max-width: 70%;
        padding: 20px 10px;
        opacity: .5;
    }

    .skill-item:not(.active-skill):hover .skill-icon {
        opacity: .8;
    }

    .active-skill .skill-icon {
        opacity: 1;
    }
    
</style>