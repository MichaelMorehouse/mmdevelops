<template>
    <div id="skills">
        <h2 class="skill-title text-uppercase">Skills and Projects</h2>
        <div id="skill-grid">
            <skill-item 
                v-for="(skill, index) in skills" 
                v-bind:key="index"
                :class="'skill' + (index + 1)"
                :skill="skill"
                v-on:activate-skill="activeSkill = skill"
            />
        </div>
        <div>
            <skill-spotlight :skill="activeSkill"></skill-spotlight>
        </div>
    </div>
</template>

<script>
import SkillItem from './SkillItem.vue'
import SkillSpotlight from './SkillSpotlight.vue'

export default {
    name: 'skill-container',
    components: {
        SkillItem,
        SkillSpotlight
    },
    data: function() {
        return {
            activeSkill: 'hi',
            skills: [
                { name: "cool guy tots", bullets: ["best cool guy pdx metro", "just the best like wow"] },
                { name: "king chill", bullets: ["top of the tops", "can he come?"]},
                { name: "smells good", bullets: ["everyone says so", "au natural"] },
                { name: "super sharp", bullets: ["mind like a steel trap", "can't get one over on this guy"]},
                { name: "C# and .NET", bullets: [".NET Framework development", "class based bs"]},
                { name: "JavaScript and Front-End", bullets: ["vanilla JS and modern syntax", "react/redux and vue.js"]}
            ]
        }
    }
}
</script>

<style>

    #skills {
        color: rgb(44, 62, 80);
        text-align: center;
        padding: 20px 10%;
    }

    .skill1 { grid-area: skillone; }
    .skill2 { grid-area: skilltwo; }
    .skill3 { grid-area: skillthree; }
    .skill4 { grid-area: skillfour; }
    .skill5 { grid-area: skillfive; }
    .skill6 { grid-area: skillsix; }

    #skill-grid {
        display: grid;
        grid-template-columns: auto auto auto;
        grid-template-rows: auto auto;
        gap: 20px;
        grid-template-areas:
            'skillone skilltwo skillthree'
            'skillfour skillfive skillsix'
        ;
    }
</style>
