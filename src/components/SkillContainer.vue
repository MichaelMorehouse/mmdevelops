<template>
  <div id="skills">
    <scroll-anchor id="skill-anchor" top="-50" left="0"/>
    <h2 id="skills-title" class="text-uppercase">Skills and Experience</h2>
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
        v-on:activate-skill="activeSkill = skill"
      />
    </div>
  </div>
</template>

<script>
import SkillItem from "./SkillItem.vue";
import SkillSpotlight from "./SkillSpotlight.vue";
import ScrollAnchor from "./ui/ScrollAnchor.vue";

export default {
  name: "skill-container",
  components: {
    SkillItem,
    SkillSpotlight,
    ScrollAnchor
  },
  data: function() {
    return {
      activeSkill: "",
      skills: [
        {
          name: "Positive Team Presence",
          bullets: [
            "Passion for learning and sharing knowledge",
            "Effective communication and diligent follow-through",
            "Responsible, accountable, and straightforward"
          ],
          icon: "team.png"
        },
        {
          name: "Data Analysis and Database Systems",
          bullets: [
            "Analytical chemistry and biostatistics background",
            "SQL, T-SQL, PostgreSQL, .NET Entity Framework",
            "MongoDB NoSQL and Mongoose ODM"
          ],
          icon: "db.png"
        },
        {
          name: "Documentation Expert",
          bullets: [
            "Consistent implementation of standard procedures and industry best practices",
            "Proficient at assembling solutions from documentation, articles and posts"
          ],
          icon: "docu.png"
        },

        {
          name: "C# and .NET, OOP",
          bullets: [
            "Well versed in Object Oriented Programming",
            "C# Some experience with C++ and Java programming",
            ".NET development with Entity Framework Code First, LINQ, ASP.NET MVC and more",
            "Azure Cloud Deployment and microservice provisioning",
            
          ],
          icon: "msnet.png"
        },
        {
          name: "Front-End JavaScript",
          bullets: [
            "Vanilla JS and modern ES6/ES7 syntax",
            "React/Redux and Vue.js"
          ],
          icon: "js.png"
        },
        {
          name: "NodeJS",
          bullets: [
            "Back-end Javascript development with ExpressJS web server",
            "Cloud application deployment using the Heroku platform"
          ],
          icon: "node.png"
        }
      ]
    };
  },
  methods: {
    skillsExist: function() {
      if (this.activeSkill == "" && this.skills[0]) {
        this.activeSkill = this.skills[0];
      }
      return this.activeSkill ? true : false;
    }
  },
  watch: {
    activeSkill: function() {
      document.getElementById("skill-anchor").scrollIntoView();
    }
  }
};
</script>

<style>
#skills {
  position: relative;
  color: rgb(44, 62, 80);
  text-align: center;
  padding: 20px 25%;
}

.skill1 {
  grid-area: skillone;
}
.skill2 {
  grid-area: skilltwo;
}
.skill3 {
  grid-area: skillthree;
}
.skill4 {
  grid-area: skillfour;
}
.skill5 {
  grid-area: skillfive;
}
.skill6 {
  grid-area: skillsix;
}

@media screen {
  #skill-grid {
    display: grid;
    grid-template-columns: 30% auto 30%;
    gap: 20px;
    grid-gap: 20px;
    justify-content: space-evenly;
    grid-template-areas:
      "skillone skilltwo skillthree"
      "skillfour skillfive skillsix";
  }
}

@media screen and (max-width: 600px) {
  #skill-grid {
    display: grid;
    grid-template-columns: auto auto;
    gap: 20px;
    grid-template-areas:
      "skill-spotlight skill-spotlight"
      "skillone skilltwo"
      "skillthree skillfour"
      "skillfive skillsix";
  }
}
</style>
