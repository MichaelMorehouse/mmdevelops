<template>
    <div id="skill-container">
        <h2 class="text-uppercase">Skills and Projects</h2>
        <div >
            <skill-item 
                v-for="skill in skills" 
                v-bind:key="skill.name"
                :name="skill.name"
                :bullets="skill.bullets"
            />
        </div>
        
    </div>
</template>

<script>
import SkillItem from './SkillItem.vue'

export default {
    name: 'skill-container',
    components: {
        SkillItem
    },
    data: function() {
        return {
            skills: [
                { name: "cool guy tots", bullets: ["best cool guy pdx metro", "just the best like wow"] },
                { name: "king chill", bullets: ["top of the tops", "can he come?"]}
            ]
        }
    }
}
</script>

<style>
    #skill-container {
        color: rgb(44, 62, 80);
        text-align: center;
        padding: 20px 10px;
    }
</style>
