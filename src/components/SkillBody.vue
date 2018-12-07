<template>
    <div id="skill-body">
        <div >
            <skill-item 
                v-for="skill in skills" 
                v-bind:key="skill.name"
                :name="skill.name"
                :description="skill.description"
            />
        </div>
        
    </div>
</template>

<script>
import SkillItem from './SkillItem.vue'

export default {
    name: 'skill-body',
    components: {
        SkillItem
    },
    data: function() {
        return {
            skills: [
                { name: "cool guy", description: "best cool guy pdx metro"},
                { name: "king chill", description: "chill like dang thats cold"}
            ]
        }
    }
}
</script>

<style>

</style>
