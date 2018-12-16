<template>
    <div id="skills">
        <h2 class="skills-title text-uppercase">Skills and Projects</h2>
        <transition name="fade">
            <skill-spotlight v-if="skillsExist()" :skill="activeSkill"></skill-spotlight>
        </transition>
        <div id="skill-grid">
            <skill-item 
                v-for="(skill, index) in skills" 
                v-bind:key="index"
                :class="'skill' + (index + 1)"
                :skill="skill"
                :isActive="skill == activeSkill"
                v-on:activate-skill="activeSkill = skill == activeSkill ? null : skill"
            />
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
            activeSkill: '',
            skills: [
                { 
                    name: "Positive Team Presence", 
                    bullets: [
                        "Passion for learning and sharing knowledge", 
                        "Effective communication and diligent follow-through",
                    ],
                    icon: 'team.png'
                },
                { 
                    name: "Documentation Enthusiast", 
                    bullets: [
                        "Quick and consistent implementation of standard procedures and best practices", 
                        "Enjoys assembling solutions from documentation, articles and posts",
                    ],
                    icon: 'docu.png'
                },
                { 
                    name: "Data Analysis and Database Systems", 
                    bullets: [
                        "Analytical chemistry and biostatistics background", 
                        "SQL, T-SQL, MS SQL Server", 
                        "MongoDB NoSQL and Mongoose ODM",
                    ],
                    icon: 'db.png'
                },
                { 
                    name: "NodeJS", 
                    bullets: [
                        "Full stack Javascript development with ExpressJS",
                        "Cloud deployment using the Heroku platform"
                    ],
                    icon: 'node.png'
                },
                { 
                    name: "C# and .NET", 
                    bullets: [
                        "ASP.NET MVC and Azure Cloud Deployment", 
                        "Entity Framework Code First, LINQ and SQL Server"
                    ],
                    icon: 'msnet.png'
                },
                { 
                    name: "Front-End JavaScript", 
                    bullets: [
                        "Vanilla JS and modern ES7 syntax", 
                        "React/Redux and Vue.js"
                    ],
                    icon: 'js.png'
                },
            ]
        }
    },
    methods: {
        skillsExist: function() {
            if (this.activeSkill == '' && this.skills[0]) {
                this.activeSkill = this.skills[0];
            }
            return this.activeSkill ? true : false;
        },
    }
}
</script>

<style>
    #skills {
        color: rgb(44, 62, 80);
        text-align: center;
        padding: 20px 15%;
    }

    skill-spotlight { grid-area: skill-spotlight; }
    .skill1 { grid-area: skillone; }
    .skill2 { grid-area: skilltwo; }
    .skill3 { grid-area: skillthree; }
    .skill4 { grid-area: skillfour; }
    .skill5 { grid-area: skillfive; }
    .skill6 { grid-area: skillsix; }

@media screen {
    #skill-grid {
        display: grid;
        grid-template-columns: 30% auto 30%;
        gap: 20px;
        grid-gap: 20px;
        grid-template-areas:
            'skill-spotlight skill-spotlight skill-spotlight'
            'skillone skilltwo skillthree'
            'skillfour skillfive skillsix'
        ;
    }
}

@media screen and (max-width: 600px) {
    #skill-grid {
        display: grid;
        grid-template-columns: auto auto;
        gap: 20px;
        grid-template-areas:
            'skill-spotlight skill-spotlight'
            'skillone skilltwo'
            'skillthree skillfour'
            'skillfive skillsix'
        ;
    }
}
</style>
